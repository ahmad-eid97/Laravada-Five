<template>
    <section class="testominials">
            <div class="row mx-0 justify-content-center">
                <h2 class="col-md-6">
                    what our clients say
                </h2>
            </div>
                
        <swiper
            :options="swiperOption"
            class="owl-carousel"
        >

            <swiper-slide>
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-12 p-0 text-center">
                            <img class="testimonial-image ls-is-cached lazyloaded" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/07/testimonials-1.jpg" width="150" height="150">
                        </div>
                        <blockquote >
                            <q class="fusion-clearfix">
                                Beauty is when you can appreciate yourself. When you love yourself, that’s when you’re most beautiful.
                            </q>
                        </blockquote>
                        <span class="company-name">
                            <strong>Shelia McCourtney,</strong>
                            ARCHITECT
                        </span>
                    </div>
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-12 p-0 text-center">
                            <img class="testimonial-image ls-is-cached lazyloaded" src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/testimonials-2.jpg" width="150" height="150">
                        </div>
                        <blockquote >
                            <q class="fusion-clearfix">
                                    "Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience."
                            </q>
                        </blockquote>
                        <span class="company-name">
                            <strong>Luis Desalvo,</strong>
                            CREO TECH
                        </span>
                    </div>
                </div>
            </swiper-slide>

        </swiper>

    </section>
</template>

<script>

export default {

    name: 'AppHomeTestominials',
    data() {
        return {
            swiperOption: {
                loop: true,
                slidesPerView: 1,
                spaceBetween: 50,
            }
        }
    }
}
</script>
<style>
    .testominials {
        padding-top: 100px;
        margin-top: 0px;
        padding-right: 30px;
        padding-bottom: 20px;
        margin-bottom: 0px;
        padding-left: 30px;
    }

    .testominials h2 {
        margin-top: 10px;
        margin-right: 0px;
        margin-bottom: 20px;
        margin-left: 0px;
        color: rgb(32, 32, 32);
        font-size: 38px;
        font-weight: 700;
        letter-spacing: -0.76px;
        line-height: 53.2px;
        text-align: center;
        text-transform: capitalize
    }

    
    .testominials .owl-carousel {
        margin-top: 30px;
        margin-bottom: 50px;
    }

    .testominials .owl-carousel .item img {
        width: 150px;
        height: 150px;
        padding: 0;
        border-radius: 50%;
        margin: 0 auto;
    }

    .testominials .owl-carousel .item blockquote {
        margin: 0;
        max-width: 900px;
    }

    .testominials .owl-carousel .item q {
        color: rgb(46, 46, 46);
        display: block;
        padding: 25px 25px 0;
        line-height: 30px;
        font-size: 18px;
        text-align: center;
        letter-spacing: 2px;
        font-style: italic;
        font-size: 18px;
        font-weight: 600;
    }
    .testominials .owl-carousel .item .company-name {
        margin-top: 25px;
        font-size: 18px;
        text-align: center;
        letter-spacing: 2px;
        color: rgb(46, 46, 46);;
    }
    .owl-theme .owl-dots .owl-dot.active span, .owl-theme .owl-dots .owl-dot:hover span {
        background: #000;
    }
    .owl-theme .owl-dots .owl-dot span {
        width: 12px;
        height: 12px;
        background: transparent;
        border: 1px solid #000
    }
</style>