<template>
  <div class="featured">
    <div class="row mx-0 justify-content-center">
      <h2 class="col-md-6">
        {{ features.find((one) => one.key === "features_title").value }}
      </h2>
    </div>
    <div class="row justify-content-center">
      <p class="col-md-6">
        {{ features.find((one) => one.key === "features_description").value }}
      </p>
    </div>
    <div
      class="row mx-0 items"
      v-if="features.find((one) => one.key === 'features_text_list').value"
    >
      <div
        v-for="feature in features
          .find((one) => one.key === 'features_text_list')
          .value.slice(0, 3)"
        :key="feature"
        class="col-md-6 col-lg-6 col-xl-4"
      >
        <div class="item">
          <div class="heading">
            <div class="icon">
              <i :class="feature.icon"></i>
            </div>
            <h3>{{ feature.title }}</h3>
          </div>
          <p>
            {{ feature.description }}
          </p>
        </div>
      </div>
    </div>
    <div class="row mx-0">
      <div class="col-12">
        <img
          src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/agency-seo-desk-front.jpg"
          class="img-fluid"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<script>
import "animate.css/animate.min.css";
export default {
  name: "AppHomeFeatured",
  props: ["features"],
  data() {
    return {};
  },
  mounted() {
    document
      .querySelector(".featured")
      .style.setProperty(
        "--features-bg",
        this.features.find(
          (one) => one.key === "features_background_active_section"
        ).value === "color"
          ? this.features.find(
              (one) => one.key === "features_background_color_section"
            ).value
          : `url(${
              this.features.find(
                (one) => one.key === "features_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".featured")
      .style.setProperty(
        "--features-fontSize",
        `${
          this.features.find((one) => one.key === "features_font_size_section")
            .value
        }px`
      );

    if (
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ) &&
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".featured")
        .style.setProperty(
          "--features-border-top",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".featured")
        .style.setProperty(
          "--features-border-bottom",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );
    } else if (
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ) &&
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".featured")
        .style.setProperty(
          "--features-border-top",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );
    } else if (
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ) &&
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ).value === "bottom"
    ) {
      document
        .querySelector(".featured")
        .style.setProperty(
          "--features-border-bottom",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>
<style lang="scss">
.featured {
  background-color: rgb(247, 248, 249);
  margin-top: 0px;
  padding-left: 30px;
  padding-right: 30px;
  padding-top: 100px;

  --features-bg: #fff;
  --features-fontSize: 20px;
  --features-border-top: 0px solid #fff;
  --features-border-bottom: 0px solid #fff;

  background: var(--features-bg);
  border-top: var(--features-border-top);
  border-bottom: var(--features-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;
  h2 {
    font-size: var(--features-fontSize);
  }
}
.featured h2 {
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
}
.featured p {
  font-size: 20px;
  font-weight: 400;
  line-height: 36px;
  margin-bottom: 20px;
  text-align: center;
}
.featured .items {
  margin-top: 0px;
  margin-bottom: 40px;
}
.featured .items .item {
  background-color: rgb(255, 255, 255);
  /* padding-bottom: 35px; */
  padding-left: 35px;
  padding-right: 35px;
  padding-top: 35px;
  margin-top: 15px;
  margin-bottom: 15px;
  height: 100%;
}
.featured .items .item .heading {
  margin-bottom: 15px;
}
.featured .items .item .icon {
  margin-bottom: 15px;
  text-align: center;
}
.featured .items .item .icon i {
  font-size: 36px;
  color: rgb(255, 167, 55);
  margin: 0 auto;
  display: block;
}
.featured .items .item h3 {
  font-size: 28px;
  font-weight: 700;
  text-align: center;
  letter-spacing: -0.56px;
  line-height: 39.2px;
}
.featured .items .item p {
  font-size: 18px;
  font-weight: 400;
  text-align: center;
  letter-spacing: -0.27px;
  line-height: 32px;
  margin-bottom: 20px;
}
.featured .items .item:hover i {
  animation: fadeInLeft 0.3s linear;
}
.featured .items .item:hover h3 {
  color: rgb(255, 167, 55);
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
