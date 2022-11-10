<template>
    <section class="partners">
                
        <swiper
            :options="swiperOption"
            class="owl-carousel"
        >

            <swiper-slide>
            <div class="item">
                <img class="" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/clients_partner_2-200x202.png" width="150" height="150">
            </div>
            </swiper-slide>

            <swiper-slide>
            <div class="item">
                <img class="" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/clients_partner_3-200x202.png" width="150" height="150">
            </div>
            </swiper-slide>

            <swiper-slide>
            <div class="item">
                <img class="" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/clients_partner_4-200x202.png" width="150" height="150">
            </div>
            </swiper-slide>

            <swiper-slide>
            <div class="item">
                <img class="" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/clients_partner_5-200x202.png" width="150" height="150">
            </div>
            </swiper-slide>

            <swiper-slide>
            <div class="item">
                <img class="" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/clients_partner_6-200x202.png" width="150" height="150">
            </div>
            </swiper-slide>

            <swiper-slide>
            <div class="item">
                <img class="" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/clients_partner_1-200x202.png" width="150" height="150">
            </div>
            </swiper-slide>

        </swiper>
    </section>
</template>

<script>
export default {
    name: 'AppHomePartners',
    data() {
        return {
            swiperOption: {
            loop: true,
            slidesPerView: 5,
            spaceBetween: 50,
            breakpoints: {
                // when window width is >= 320px
                100: {
                slidesPerView: 1,
                spaceBetween: 5,
                },
                // when window width is >= 480px
                480: {
                slidesPerView: 2,
                spaceBetween: 5,
                },
                // when window width is >= 640px
                640: {
                slidesPerView: 3,
                spaceBetween: 5,
                },
                992: {
                slidesPerView: 4,
                spaceBetween: 5,
                },
                1200: {
                slidesPerView: 5,
                spaceBetween: 5,
                },
            }
            },
        }
    }
}
</script>
<style>
    section.partners {
        padding: 0 30px 30px;
    }
    section.partners .owl-carousel {
        padding-top: 50px;
        border-top: 1px solid #e8eaf0;
    }
    section.partners .owl-carousel .item  {
        text-align: center;
    }
    section.partners .owl-carousel .item img {
        max-height: 115px;
        vertical-align: middle;
        width: auto;
        display: inline;
    }


</style>