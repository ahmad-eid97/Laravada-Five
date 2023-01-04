<template>
  <header>
    <div class="cart" :class="openCart ? 'opened' : ''">
      <div class="head">
        <i class="fa-regular fa-xmark" @click="openCart = false"></i>
        <button
          @click="goToCheckout"
          :disabled="$store.state.cartItems.length <= 0"
        >
          <i class="fa-regular fa-badge-check"></i> Checkout
        </button>
      </div>
      <cart />
    </div>
    <b-navbar toggleable="lg justify-content-between">
      <b-navbar-brand :href="localePath('/')">
        <img src="/assets/images/logo.png" alt="logoImage" />
      </b-navbar-brand>

      <div class="d-flex align-items-center optionsWrapper">
        <b-navbar-toggle target="navbar-toggle-collapse">
          <template #default="{ expanded }">
            <span
              class="menu-trigger"
              :class="expanded ? 'active' : ''"
              id="menu03"
            >
              <span></span>
              <span></span>
              <span></span>
            </span>
          </template>
        </b-navbar-toggle>

        <div class="d-flex align-items-center smallScr">
          <langSwitch></langSwitch>
          <div class="m-0 cartIcon" @click="openCart = !openCart">
            <span>{{ $store.state.cartItems.length }}</span>
            <i class="fa-regular fa-cart-plus"></i>
          </div>
          <div v-if="$store.state.user" class="logout" @click="logout">
            <i class="fa-regular fa-right-from-bracket"></i>
          </div>
        </div>
      </div>
      <b-collapse
        id="navbar-toggle-collapse"
        class="ml-auto justify-content-between"
        is-nav
      >
        <b-navbar-nav class="align-items-center">
          <b-nav-item :to="localePath('/')" active-class="active" exact
            >Who We Are</b-nav-item
          >
          <b-nav-item :to="localePath('/about')" active-class="active"
            >What We Do</b-nav-item
          >
          <b-nav-item :to="localePath('/testimonials')" active-class="active"
            >Where We Work</b-nav-item
          >
          <b-nav-item :to="localePath('/services')" active-class="active"
            >Careers</b-nav-item
          >
          <b-nav-item :to="localePath('/blogs')" active-class="active"
            >News</b-nav-item
          >
          <b-nav-item :to="localePath('/careers')" active-class="active"
            >Career</b-nav-item
          >
          <b-nav-item :to="localePath('/events')" active-class="active"
            >Events</b-nav-item
          >
          <b-nav-item
            :to="localePath('/logout')"
            v-if="$store.state.user"
            @click="logout"
            class="outLarge"
            >Logout</b-nav-item
          >
        </b-navbar-nav>
        <div class="d-flex align-items-center">
          <a href="#" class="btn">Get in touch now</a>

          <div class="d-flex align-items-center largeScr">
            <langSwitch></langSwitch>
            <div class="m-0 cartIcon" @click="openCart = !openCart">
              <span>{{ $store.state.cartItems.length }}</span>
              <i class="fa-regular fa-cart-plus"></i>
            </div>
            <div v-if="$store.state.user" class="logout" @click="logout">
              <i class="fa-regular fa-right-from-bracket"></i>
            </div>
          </div>
        </div>
      </b-collapse>
    </b-navbar>
  </header>
</template>

<script>
import cart from "../cart/cart.vue";
import langSwitch from "../langSwitch/langSwitch.vue";
// import DropdownMenu from '@innologica/vue-dropdown-menu'
export default {
  name: "AppHeader",
  components: {
    langSwitch,
    cart,
    // DropdownMenu
  },
  data() {
    return {
      show: false,
      show1: false,
      topOfPage: true,
      openCart: false,
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  mounted() {},
  methods: {
    logout() {
      this.$swal({
        title: "Logout!",
        text: "Are you sure? You want to logout from your account!",
        type: "warning",
        showCancelButton: true,
        confirmButtonColor: "#ff5e57",
        confirmButtonText: "Logout",
      }).then((result) => {
        // <--
        if (result.value) {
          // <-- if confirmed
          this.confirmLogout();
        }
      });
    },
    confirmLogout() {
      this.$store.commit("setUserData", null);
      this.$cookies.remove("cms-auth");
      this.$cookies.remove("cms-user");
      this.$router.push(this.localePath("/login"));
    },
    handleScroll() {
      if (window.pageYOffset > 200) {
        if (this.topOfPage) this.topOfPage = false;
      } else {
        if (!this.topOfPage) this.topOfPage = true;
      }
    },
    goToCheckout() {
      this.openCart = false;
      this.$router.push("/checkout");
    },
  },
};
</script>
<style lang="scss">
.swal2-container {
  padding: 0 !important;
}
.swal2-shown {
  padding: 0 !important;
}
.swal2-confirm:focus,
.swal2-cancel:focus {
  box-shadow: none !important;
}
.swal2-cancel {
  background: #e5e5e5 !important;
  color: rgb(51, 51, 51) !important;
}
header {
  padding-top: 12px;
  margin-top: 0px;
  padding-right: 30px;
  padding-bottom: 12px;
  margin-bottom: 0px;
  padding-left: 30px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
  max-height: 80px;
  /* background: transparent !important; */
  /* position: absolute;
        left: 0;
        right: 0; */
  background: var(--main-background);
  @include sm {
    padding-right: 10px;
    padding-left: 10px;
  }
  .cart {
    width: 390px;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    transform: translateX(390px);
    background-color: #fff;
    z-index: 999999;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
    .head {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 10px;
      & > i {
        border: 1px solid var(--main-color);
        border-radius: 5px;
        width: 30px;
        height: 30px;
        display: grid;
        place-items: center;
        cursor: pointer;
        background-color: var(--main-color);
        color: #fff;
        &:hover {
          color: var(--main-color);
          background: transparent;
        }
      }
      button {
        padding: 5px 30px;
        font-size: 1.1rem;
        background-color: var(--main-color);
        color: #fff;
        border: 1px solid var(--main-color);
        display: flex;
        align-items: center;
        gap: 5px;
        i {
          font-size: 1.1rem;
        }
        &:disabled {
          opacity: 0.5;
          cursor: not-allowed;
          &:hover {
            background-color: var(--main-color);
            color: #fff;
          }
        }
        &:hover {
          background-color: transparent;
          color: var(--main-color);
        }
      }
    }
    &.opened {
      transform: translateX(0);
    }
    @include xs {
      width: 350px;
    }
  }
  .cartIcon {
    border: 1px solid #fff;
    border-radius: 5px;
    width: 45px;
    height: 45px;
    display: grid;
    place-items: center;
    cursor: pointer;
    position: relative;
    span {
      position: absolute;
      top: -15px;
      right: -10px;
      width: 30px;
      height: 30px;
      background-color: var(--main-color);
      border-radius: 50%;
      color: #fff;
      display: grid;
      place-content: center;
      font-size: 1.2rem;
    }
    i {
      color: #fff;
    }
    @include sm {
      width: 40px;
      height: 40px;
      margin: 0 10px !important;
    }
    &:hover {
      background-color: var(--main-color);
      border-color: var(--main-color);
      i {
        color: #fff;
      }
    }
  }
  .logout {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: var(--main-color);
    color: #fff;
    display: grid;
    place-items: center;
    font-size: 1.2rem;
    cursor: pointer;
    margin: 0 20px;
    @include md {
      display: none;
    }
  }
  .largeScr {
    display: flex !important;
    @include md {
      display: none !important;
    }
  }
  .smallScr {
    display: none !important;
    @include md {
      display: flex !important;
    }
  }
  .outLarge {
    display: none;
    @include md {
      display: inline;
    }
  }
}
.optionsWrapper {
  @include md {
    flex-direction: row-reverse;
  }
}
.navbar-brand {
  padding-top: 0px !important;
  padding-right: 0px !important;
  margin-right: 25px;
  padding-bottom: 0px !important;
  padding-left: 0px !important;
}

.logout {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: var(--main-color);
  color: #fff;
  display: grid;
  place-items: center;
  font-size: 1.2rem;
  cursor: pointer;
}
.navbar-brand img {
  max-width: 162px;
  height: auto;
}
.nav-item {
  position: relative;
  margin-right: 16px;
  justify-content: center;
  transition: all calc(300 * 1ms) cubic-bezier(0.42, 0.01, 0.58, 1);
  font-size: 16px;
}
.navbar-nav .nav-link.active {
  color: rgb(255, 167, 55);
}
.nav-link {
  font-weight: 400;
  font-size: 16px;
  line-height: 29px;
  color: #fff;
}
.active .nav-link,
.nav-link:hover {
  color: rgb(255, 167, 55);
}

.navbar-toggler,
.navbar-toggler:focus {
  border: none;
  box-shadow: none;
  margin: 0;
}
.menu-trigger,
.menu-trigger span {
  display: inline-block;
  transition: all 0.4s;
  box-sizing: border-box;
}
.menu-trigger {
  position: relative;
  width: 32px;
  height: 25px;
  background: none;
  border: none;
  appearance: none;
  cursor: pointer;
}
.menu-trigger span {
  position: absolute;
  left: 0;
  width: 100%;
  height: 5px;
  background-color: #fff;
  border-radius: 4px;
}
.menu-trigger span:nth-of-type(1) {
  top: 0;
}
.menu-trigger span:nth-of-type(2) {
  top: 10px;
}
.menu-trigger span:nth-of-type(3) {
  bottom: 0;
}
#menu03.active {
  transform: rotate(360deg);
}
#menu03.active span:nth-of-type(1) {
  transform: translateY(10px) rotate(-45deg);
}
#menu03.active span:nth-of-type(2) {
  transform: translateY(0) rotate(45deg);
}
#menu03.active span:nth-of-type(3) {
  opacity: 0;
}

nav .btn {
  border-radius: 25px 25px 25px 25px;
  padding-bottom: 13px;
  padding-left: 29px;
  padding-right: 29px;
  padding-top: 13px;
  font-weight: 700;
  justify-content: center;
  letter-spacing: 0.21px;
  font-size: 14px;
  color: rgb(255, 255, 255);
  background-color: #ffa737;
  line-height: 17px;
  min-width: 200px;
  text-transform: uppercase;
}

nav .btn:hover {
  color: rgb(255, 255, 255);
  border-color: #fff;
}

@include md {
  nav .btn {
    display: none;
  }
}

@media screen and (max-width: 991px) {
  .navbar-collapse.show .navbar-nav {
    position: absolute;
    width: 250px;
    top: 56px;
    right: 0;
  }
  .nav-item {
    width: 100%;
    border-bottom: 1px solid #e5e5e5;
    background: #fff;
  }
  .nav-item .nav-link {
    color: #000;
  }
  .nav-item:after {
    content: none;
  }
  .nav-item.active,
  .nav-item:hover {
    background-color: rgb(255, 167, 55);
  }
  .nav-item.active .nav-link,
  .nav-item:hover .nav-link {
    color: #fff;
  }
  .nav-link {
    padding: 8px 20px !important;
    font-weight: 800;
    font-size: 15px;
    text-align: right;
  }
}
</style>
