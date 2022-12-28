<template>
  <section class="intro">
    <VueSlickCarousel :arrows="true" :fade="true" :dots="false">
      <div class="item item-1">
        <div class="row h-100 m-0 align-items-center">
          <div class="col-md-6">
            <h1>
              We Provide The <br />
              Best Seo Services
            </h1>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              <br />
              Phasellus eu ornare erat. Curabitur pulvinar elit.
            </p>
            <a href="#" class="btn">BUY LARAVADA NOW</a>
            <a href="#" class="btn blue">CONTACT US</a>
          </div>
          <div class="col-md-6">
            <img
              src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/best-seo-services-slide-1.png"
              alt=""
            />
          </div>
        </div>
      </div>
      <div class="item item-2">
        <div class="row h-100 m-0 align-items-center">
          <div class="col">
            <h1>
              SEM Campaigns Made<br />
              Simple With laravada
            </h1>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              <br />
              Phasellus eu ornare erat. Curabitur pulvinar elit.
            </p>
          </div>
          <div class="col">
            <img
              src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/best-sem-seo-services-slide-2.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </VueSlickCarousel>
  </section>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
import "animate.css/animate.css";
export default {
  name: "AppHomeIntro",
  props: ["sliderData"],
  components: {
    VueSlickCarousel,
  },
  data() {
    return {};
  },
  mounted() {
    console.log(this.sliderData);
  },
};
</script>
<style lang="scss">
.intro .item-1 {
  background: rgb(10, 14, 124);
  background: linear-gradient(
    145deg,
    rgba(10, 14, 124, 1) 0%,
    rgba(83, 38, 170, 1) 100%
  );
  width: 100%;
  min-height: 100vh;
  position: relative;
}
.intro .item-2 {
  background: rgb(50, 27, 91);
  background: linear-gradient(
    145deg,
    rgba(50, 27, 91, 1) 0%,
    rgba(137, 54, 89, 1) 50%,
    rgba(235, 133, 76, 1) 100%
  );
  width: 100%;
  min-height: 100vh;
  position: relative;
}
.intro .item .row {
  min-height: 100vh;
  padding: 150px 50px 0;
}
.intro .item h1 {
  font-size: 55px;
  color: #fff;
  font-weight: 700;
}
.intro .item p {
  font-size: 20px;
  color: #fff;
  font-weight: 400;
}

@include xs {
  .intro .item h1 {
    font-size: 35px;
  }
  .intro .item p {
    font-size: 17px;
  }
}

.slick-prev::before,
.slick-next::before {
  font-family: "slick";
  font-size: 20px;
  line-height: 1;
  opacity: 0.75;
  color: #fff;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #000;
  padding: 10px;
}

.slick-prev {
  left: 0;
  z-index: 2;
}
.slick-next {
  right: 20px;
}
.item .btn {
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
  text-transform: uppercase;
  display: inline-block;
  margin: 0 10px 10px;
}
.item .btn.blue {
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
  background-color: rgb(85, 110, 237);
  line-height: 17px;
  text-transform: uppercase;
  display: inline-block;
  margin: 0 10px;
}

.slick-active .item h1 {
  animation: fadeInLeft;
  animation-duration: 2s;
}
.slick-active .item p {
  animation: fadeInLeft;
  animation-duration: 3s;
}
.slick-active .item .btn {
  animation: fadeInUp;
  animation-duration: 4s;
}
.slick-active .item .btn.blue {
  animation: fadeInUp;
  animation-duration: 5s;
}
.slick-active .item img {
  animation: fadeIn;
  animation-duration: 5s;
}
</style>
