<template>
  <div class="home">
    <app-home-intro :slides="slides"></app-home-intro>
    <app-home-featured :features="features"></app-home-featured>
    <app-home-featured-2 :services="services"></app-home-featured-2>
    <app-home-work :projects="projects"></app-home-work>
    <app-home-plans></app-home-plans>
    <app-home-news :blogs="blogs"></app-home-news>
    <app-home-activities :activities="activities" />
    <app-home-steps :steps="steps" />
    <app-home-testominials :testimonials="testimonials"></app-home-testominials>
    <app-home-partners :partners="partners"></app-home-partners>
    <app-home-bottom-banner
      :bottomBanner="bottomBanner"
    ></app-home-bottom-banner>
    <!-- <app-home-features></app-home-features>
    <app-home-work></app-home-work> -->
  </div>
</template>

<script>
import AppHomeBottomBanner from "../components/home/AppHomeBottomBanner.vue";
import AppHomeFeatured from "../components/home/AppHomeFeatured.vue";
import AppHomeFeatured2 from "../components/home/AppHomeFeatured2.vue";
import AppHomeNews from "../components/home/AppHomeNews.vue";
import AppHomePlans from "../components/home/AppHomePlans.vue";
import AppHomeTestominials from "../components/home/AppHomeTestominials.vue";
import AppHomeIntro from "../components/home/AppHomeIntro.vue";
import AppHomeWork from "../components/home/AppHomeWork.vue";
import AppHomePartners from "../components/home/AppHomePartners.vue";
import AppHomeActivities from "../components/home/AppHomeActivities.vue";
import AppHomeSteps from "../components/home/AppHomeSteps.vue";

export default {
  name: "Home",
  components: {
    AppHomeIntro,
    AppHomeFeatured,
    AppHomeWork,
    AppHomeFeatured2,
    AppHomePlans,
    AppHomeNews,
    AppHomeTestominials,
    AppHomePartners,
    AppHomeBottomBanner,
    AppHomeActivities,
    AppHomeSteps,
  },
  async asyncData({ $axios, app }) {
    const slides = await $axios.get("/sliders", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const features = await $axios.get("/sections/features", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const projects = await $axios.get("/portfolios");

    const services = await $axios.get("/services");

    const blogs = await $axios.get("/blogs?latest=1");

    const testimonials = await $axios.get("/testimonials");

    const partners = await $axios.get("/partners");

    const bottomBanner = await $axios.get("/sections/banner-bottom", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const activities = await $axios.get("/sections/activities", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const steps = await $axios.get("/sections/steps", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    return {
      slides: slides.data.data.sliders,
      features: features.data.data,
      projects: projects.data.data.portfolios,
      services: services.data.data.services,
      blogs: blogs.data.data.blogs.slice(0, 3),
      testimonials: testimonials.data.data.testimonials,
      partners: partners.data.data.partners,
      bottomBanner: bottomBanner.data.data,
      activities: activities.data.data,
      steps: steps.data.data,
    };
  },
};
</script>
<style></style>
