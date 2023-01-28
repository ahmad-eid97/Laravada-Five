<template>
  <footer>
    <subscribe />
    <div class="row justify-content-center">
      <div class="col-auto">
        <img
          :src="
            $store.state.websiteSettings.find((one) => one.key === 'logo')
              .plain_value
          "
          alt="logoImage"
        />
      </div>
    </div>
    <b-navbar-nav
      class="align-items-center justify-content-center line footerLinks"
    >
      <nuxt-link
        v-for="page in $store.state.footerPages"
        :key="page.id"
        :to="localePath(generatePagePath(page.id))"
      >
        {{ page.name }}
      </nuxt-link>
      <!-- <nuxt-link :to="localePath('/contact')">Contact</nuxt-link>
      <nuxt-link :to="localePath('/faq')">FAQs</nuxt-link>
      <nuxt-link :to="localePath('/policy')">Privacy Policy</nuxt-link>
      <nuxt-link :to="localePath('/terms')">Terms & Conditions</nuxt-link> -->
    </b-navbar-nav>
    <div class="row mx-0 justify-content-center">
      <div class="col-auto copyright">
        <p>
          © Copyright 2023&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;Laravada
          Theme&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;All Rights
          Reserved&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;Powered by
          <a href="http://wordpress.org" target="_blank" rel="noreferrer"
            >Rail Coder</a
          >
        </p>
      </div>
    </div>
    <div class="row mx-0 align-items-center justify-content-center">
      <div class="col-auto social">
        <a
          :href="`https://${$store.state.footerData.facebook}`"
          target="_blank"
        >
          <i class="fa-brands fa-facebook-f"></i>
        </a>
        <!-- <a :href="$store.state.footerData.twitter" >
                    <i icon="fa-brands fa-twitter" />
                </a> -->
        <a :href="`https://${$store.state.footerData.youtube}`" target="_blank">
          <i class="fa-brands fa-youtube"></i>
        </a>
        <a
          :href="`https://${$store.state.footerData.instagram}`"
          target="_blank"
        >
          <i class="fa-brands fa-instagram"></i>
        </a>
        <a
          :href="`https://${$store.state.footerData.linkedin}`"
          target="_blank"
        >
          <i class="fa-brands fa-linkedin-in"></i>
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
import Subscribe from "../subscribe/subscribe.vue";
export default {
  name: "AppFooter",
  components: { Subscribe },
  data() {
    return {};
  },
  methods: {
    generatePagePath(id) {
      switch (id) {
        case 1:
          return "/about";
        case 2:
          return "/contact";
        case 3:
          return "/terms";
        case 4:
          return "/policy";
      }
    },
  },
  mounted() {
    console.log(this.$store.state.footerData);
  },
};
</script>
<style lang="scss">
footer {
  /* padding-top: 48px; */
  margin-top: 0px;
  /* padding-right: 30px; */
  padding-bottom: 48px;
  margin-bottom: 0px;
  /* padding-left: 30px; */
}

footer img {
  margin-right: 24px;
  padding-top: 46px;
  width: 200px;
}

footer .navbar-nav {
  flex-direction: row;
}
footer .navbar-nav .nav-item {
  padding: 25px 20px;
}
footer .navbar-nav .nav-link {
  color: rgb(33, 41, 52);
}
footer .nav-link.active,
footer .nav-link:hover {
  color: rgb(255, 167, 55);
}

footer .copyright {
  font-size: 13px;
  color: rgb(93, 95, 100);
  font-weight: 400;
  letter-spacing: 0.27px;
  line-height: 23.4px;
}
footer .copyright a {
  color: rgb(255, 167, 55);
  text-decoration: none;
}
footer .social a {
  color: rgb(93, 95, 100);
  cursor: pointer;
  display: inline-block;
  font-size: 20px;
  margin: 10px;
}
@include sm {
  .line li {
    padding-right: 0 !important;
    padding-left: 0 !important;
  }
}
@include xs {
  .line {
    display: block;
  }
  .line li {
    padding: 0 !important;
  }
}
</style>
