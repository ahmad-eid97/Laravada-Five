<template>
  <section class="intro">
    <VueSlickCarousel :arrows="true" :fade="true" :dots="false">
      <div class="item item-1" v-for="slide in slides" :key="slide.id">
        <div class="row h-100 m-0 align-items-center">
          <div class="col-md-6">
            <h1>
              {{ slide.title }}
            </h1>
            <p>
              {{ slide.description }}
            </p>
            <a :href="slide.link" class="btn">LEARN MORE</a>
          </div>
          <div class="col-md-6">
            <img :src="slide.image" alt="" />
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
  props: ["slides"],
  components: {
    VueSlickCarousel,
  },
  data() {
    return {};
  },
  mounted() {
    console.log(this.slides);
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
  cursor: pointer;
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
