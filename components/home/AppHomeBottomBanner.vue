<template>
    <div class="banner-bottom">
       <div class="row mx-0 justify-content-center">
            <h2 class="col-md-6">
                start your free consultation
            </h2>
        </div>
        <div class="row justify-content-center">
            <p class="col-md-6 lead">
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.
            </p>
        </div>
        <div class="row mx-0 mt-5 align-items-center justify-content-center">
            <div class="col-auto">
                <a href="#" class="btn">CONTACT US NOW</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppHomeBanner',
    data() {
        return {

        }
    }
}
</script>
<style>
    .banner-bottom {
        background-blend-mode: overlay;
        background-color: rgba(0, 0, 0, 0.6);
        background-image: url("https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/CTA-seo-1.jpg");
        background-position-x: 50%;
        background-position-y: 50%;
        background-repeat: no-repeat;
        background-size: cover;
        padding: 60px 30px;
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