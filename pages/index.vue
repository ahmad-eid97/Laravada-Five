<template>
  <div class="home">
    <app-home-intro></app-home-intro>
    <app-home-featured></app-home-featured>
    <app-home-featured-2></app-home-featured-2>
    <app-home-work></app-home-work>
    <app-home-plans></app-home-plans>
    <app-home-news></app-home-news>
    <app-home-testominials></app-home-testominials>
    <app-home-partners></app-home-partners>
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
  }
}
</script>
<style>
  
</style>