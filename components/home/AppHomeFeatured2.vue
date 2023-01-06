<template>
  <div class="featured2">
    <div class="row mx-0 justify-content-center">
      <h2 class="col-md-6">see our top notch services</h2>
    </div>
    <div class="row mx-0 justify-content-center">
      <p class="col-md-6">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium.
      </p>
    </div>
    <div class="row items mx-0" v-if="services">
      <div
        v-for="service in services.slice(0, 4)"
        :key="service"
        class="col-md-6 col-lg-6 col-xl-3 service"
      >
        <div class="item">
          <div class="heading">
            <div class="icon">
              <i class="fa-brands fa-google"></i>
            </div>
            <h3>{{ service.title }}</h3>
          </div>
          <p>
            {{ service.short_description }}
          </p>
          <nuxt-link :to="`/service/${service.id}`"
            >Let's work together <i class="fa-solid fa-angle-right"></i
          ></nuxt-link>
        </div>
      </div>
      <button class="services" @click="$router.push('/services')">
        SEE SERVICES
      </button>
    </div>
  </div>
</template>

<script>
import "animate.css/animate.min.css";
export default {
  name: "AppHomeFeatured2",
  props: ["services"],
  data() {
    return {};
  },
};
</script>
<style>
.featured2 {
  background-color: rgb(0, 12, 71);
  background-position: center center;
  background-repeat: no-repeat;
  border-width: 0px;
  border-color: var(--awb-color3);
  border-style: solid;
  background-size: cover;
  background-image: url("https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/pattern_background.png");
  padding-bottom: 85.4px;
  padding-left: 30px;
  padding-right: 30px;
  padding-top: 100px;
}
.featured2 h2 {
  margin-top: 10px;
  margin-right: 0px;
  margin-bottom: 20px;
  margin-left: 0px;
  font-size: 38px;
  font-weight: 700;
  letter-spacing: -0.76px;
  line-height: 53.2px;
  text-align: center;
  text-transform: capitalize;
  color: #fff;
}
.featured2 p {
  font-size: 20px;
  font-weight: 400;
  line-height: 36px;
  margin-bottom: 20px;
  text-align: center;
  color: #fff;
}
.featured2 .items {
  margin-top: 60px;
  margin-bottom: 20px;
}
.featured2 .items .item {
  background-color: rgb(0, 16, 97);
  padding-bottom: 35px;
  padding-left: 35px;
  padding-right: 35px;
  padding-top: 35px;
  margin-top: 15px;
  margin-bottom: 20px;
  height: 100%;
}
.featured2 .items .item .heading {
  margin-bottom: 15px;
}
.featured2 .items .item .icon {
  margin-bottom: 15px;
  text-align: center;
}
.featured2 .items .item .icon i {
  font-size: 36px;
  color: rgb(255, 167, 55);
  margin: 0 auto;
  display: block;
}
.featured2 .items .item h3 {
  font-size: 28px;
  font-weight: 700;
  text-align: center;
  letter-spacing: -0.56px;
  line-height: 39.2px;
  color: #fff;
}
.featured2 .items .item p {
  font-size: 18px;
  font-weight: 400;
  text-align: center;
  letter-spacing: -0.27px;
  line-height: 32px;
  margin-bottom: 20px;
  color: #fff;
}
.featured2 .items .item:hover .icon i {
  animation: fadeInLeft 0.3s linear;
}
.featured2 .items .item:hover h3 {
  color: rgb(255, 167, 55);
}
.featured2 a {
  color: rgb(255, 167, 55);
  text-align: center;
  text-decoration: none;
  display: block;
}

button.services {
  margin: 50px auto 0 !important;
  width: 200px !important;
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

button:hover {
  background: transparent;
  border-color: #fff;
}

@-webkit-keyframes fadeInLeft {
  from {
    opacity: 0;
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }

  to {
    opacity: 1;
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}
</style>
