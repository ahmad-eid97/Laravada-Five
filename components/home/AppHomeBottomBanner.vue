<template>
  <div class="banner-bottom">
    <div class="overlay"></div>
    <div class="row mx-0 justify-content-center">
      <h2 class="col-md-6">
        {{
          bottomBanner.find((one) => one.key === "banner-bottom_title").value
        }}
      </h2>
    </div>
    <div class="row justify-content-center">
      <p class="col-md-6 lead">
        {{
          bottomBanner.find((one) => one.key === "banner-bottom_description")
            .value
        }}
      </p>
    </div>
    <div class="row mx-0 mt-5 align-items-center justify-content-center">
      <div class="col-auto">
        <a
          :href="
            bottomBanner.find((one) => one.key === 'banner-bottom_link').value
          "
          class="btn"
          >CONTACT US NOW</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHomeBanner",
  props: ["bottomBanner"],
  data() {
    return {};
  },
  mounted() {
    document
      .querySelector(".banner-bottom")
      .style.setProperty(
        "--bannerBottom-bg",
        this.bottomBanner.find(
          (one) => one.key === "banner-bottom_background_active_section"
        ).value === "color"
          ? this.bottomBanner.find(
              (one) => one.key === "banner-bottom_background_color_section"
            ).value
          : `url(${
              this.bottomBanner.find(
                (one) => one.key === "banner-bottom_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".banner-bottom")
      .style.setProperty(
        "--bannerBottom-fontSize",
        `${
          this.bottomBanner.find(
            (one) => one.key === "banner-bottom_font_size_section"
          ).value
        }px`
      );

    if (
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ) &&
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".banner-bottom")
        .style.setProperty(
          "--bannerBottom-border-top",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".banner-bottom")
        .style.setProperty(
          "--bannerBottom-border-bottom",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );
    } else if (
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ) &&
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".banner-bottom")
        .style.setProperty(
          "--bannerBottom-border-top",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );
    } else if (
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ) &&
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".banner-bottom")
        .style.setProperty(
          "--bannerBottom-border-bottom",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>
<style lang="scss">
.banner-bottom {
  background-blend-mode: overlay;
  background-color: rgba(0, 0, 0, 0.6);
  /* background-image: url("https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/CTA-seo-1.jpg"); */
  background-position-x: 50%;
  background-position-y: 50%;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 60px 30px;
  position: relative;

  --bannerBottom-bg: #fff;
  --bannerBottom-fontSize: 20px;
  --bannerBottom-border-top: 0px solid #fff;
  --bannerBottom-border-bottom: 0px solid #fff;

  background: var(--bannerBottom-bg);
  border-top: var(--bannerBottom-border-top);
  border-bottom: var(--bannerBottom-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;
  h2 {
    font-size: var(--bannerBottom-fontSize);
  }
}
h2,
p,
a {
  position: relative;
  z-index: 9;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
}
.banner-bottom h2 {
  margin: 50px 0 20px;
  color: rgb(255, 255, 255);
  font-size: 38px;
  font-weight: 700;
  letter-spacing: -0.76px;
  line-height: 53.2px;
  text-align: center;
}
.banner-bottom p {
  margin: 0 0 60px;
  color: rgb(255, 255, 255);
  font-size: 20px;
  font-weight: 400;
  line-height: 36px;
  text-align: center;
}
.banner-bottom .btn {
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
}
</style>
