<template>
  <div class="heading">
    <div class="row justify-content-center m-0">
      <h3 class="col-12 text-center title">Service Details</h3>
      <div class="col-12 text-center">
        <div class="breadcrumb">
          <router-link :to="localePath('/')"> Home </router-link>
          <a href="">
            <i class="fa-solid fa-angles-right"></i>
          </a>
          <nuxt-link :to="localePath('/services')"> Services </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppServiceHeading",
};
</script>

<style></style>
