<template>
  <div class="home">
    <app-home-intro :sliderData="sliderData"></app-home-intro>
    <app-home-featured></app-home-featured>
    <app-home-featured-2 :services="services"></app-home-featured-2>
    <app-home-work></app-home-work>
    <app-home-plans></app-home-plans>
    <app-home-news :blogs="blogs"></app-home-news>
    <app-home-testominials :testimonials="testimonials"></app-home-testominials>
    <app-home-partners :partners="partners"></app-home-partners>
    <app-home-bottom-banner></app-home-bottom-banner>
    <!-- <app-home-features></app-home-features>
    <app-home-work></app-home-work> -->
  </div>
</template>

<script>
import AppHomeBottomBanner from '../components/home/AppHomeBottomBanner.vue'
import AppHomeFeatured from '../components/home/AppHomeFeatured.vue'
import AppHomeFeatured2 from '../components/home/AppHomeFeatured2.vue'
import AppHomeNews from '../components/home/AppHomeNews.vue'
import AppHomePlans from '../components/home/AppHomePlans.vue'
import AppHomeTestominials from '../components/home/AppHomeTestominials.vue'
import AppHomeIntro from '../components/home/AppHomeIntro.vue'
import AppHomeWork from '../components/home/AppHomeWork.vue'
import AppHomePartners from '../components/home/AppHomePartners.vue'

export default {
  name: 'Home',
  components: {
    AppHomeIntro,
    AppHomeFeatured,
    AppHomeWork,
    AppHomeFeatured2,
    AppHomePlans,
    AppHomeNews,
    AppHomeTestominials,
    AppHomePartners,
    AppHomeBottomBanner
  },
  async asyncData({ $axios }) {
    const sliderData = await $axios.get('/sliders');

    const services = await $axios.get('/services');

    const blogs = await $axios.get('/blogs?latest=1');

    const testimonials = await $axios.get('/testimonials');

    const partners = await $axios.get('/partners');

    return {
      sliderData: sliderData.data.data.sliders,
      services: services.data.data.services,
      blogs: blogs.data.data.blogs,
      testimonials: testimonials.data.data.testimonials,
      partners: partners.data.data.partners
    }
  }
}
</script>
<style>
  
</style>