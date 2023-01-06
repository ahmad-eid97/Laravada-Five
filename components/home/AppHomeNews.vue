<template>
  <section class="news">
    <div class="row mx-0 justify-content-center">
      <h2 class="col-md-6">latest news</h2>
    </div>
    <div class="row justify-content-center">
      <p class="col-md-6 lead">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium.
      </p>
    </div>
    <div class="row justify-content-between m-0" v-if="blogs.length">
      <div
        v-for="blog in blogs"
        :key="blog.id"
        class="col-md-6 col-lg-6 col-xl-4"
      >
        <div class="new">
          <div class="image">
            <img :src="blog.image" alt="" />
          </div>
          <div class="content">
            <h2>
              <a href="#">
                {{ blog.title }}
              </a>
            </h2>
            <p class="meta">
              <span>{{ blog.publish_date }}</span>
            </p>
            <p class="text">
              {{ blog.short_description }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="row mx-0 mt-5 align-items-center justify-content-center">
      <div class="col-auto">
        <nuxt-link :to="`/blogs`" class="btn">Go To News</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeNews",
  props: ["blogs"],
  data() {
    return {};
  },
};
</script>
<style>
.news {
  padding-top: 100px;
  margin-top: 0;
  padding-right: 30px;
  padding-bottom: 80px;
  margin-bottom: 0px;
  padding-left: 30px;
  background-color: rgb(247, 248, 249);
}

.news h2 {
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
.news .lead {
  font-size: 20px;
  font-weight: 400;
  line-height: 36px;
  margin-bottom: 60px;
  text-align: center;
}

.news .image img {
  width: 100%;
  opacity: 1;
  transition: opacity 1s, transform 1s;
}

.news .new {
  overflow: hidden;
}

.news .image:hover img {
  opacity: 0.9;
  transform: scale3d(1.1, 1.1, 1);
}

.news .new .content h2 {
  font-size: 24px;
  text-align: center;
  font-weight: 700;
  letter-spacing: -0.48px;
  line-height: 33.6px;
  margin: 15px 0 3px;
}
.news .new .content h2 a {
  text-decoration: none;
  color: rgb(255, 167, 55);
}
.news .new .content .meta {
  font-size: 14px;
  color: rgb(93, 95, 100);
  font-weight: 400;
  line-height: 21px;
  text-align: center;
  letter-spacing: 0.27px;
}

.news .new .content .text {
  color: rgb(93, 95, 100);
  font-size: 18px;
  font-weight: 400;
  letter-spacing: 0.27px;
  line-height: 32.4px;
  text-align: center;
}

.news .btn {
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
