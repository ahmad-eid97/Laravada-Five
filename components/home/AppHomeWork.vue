<template>
    <section class="work">
        <div class="row mx-0 justify-content-center">
            <h2 class="col-md-6">
                our work
            </h2>
        </div>
        <div class="row justify-content-center">
            <p class="col-md-6">
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.
            </p>
        </div>
        <div class="row">
            <CoolLightBox 
                :items="items" 
                :index="index"
                @close="index = null">
            </CoolLightBox>
            <div class="images-wrapper">
                <div class="row justify-content-between m-0">
                    <div
                        class="col-md-6 col-lg-6 col-xl-4 my-3"
                        v-for="(image, imageIndex) in items"
                        :key="imageIndex"
                        @click="index = imageIndex"
                    >
                        <div class="image" :style="{ backgroundImage: 'url(' + image + ')' }">
                            <div class="rollover">
                                <div class="rollover-content">
                                    <a class="rollover-link" href="#">
                                        <font-awesome-icon icon="fa-solid fa-link" />
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="row mx-0 mt-5 justify-content-center">
            <div class="col-auto">
                <a href="#" class="btn">VIEW ALL WORK</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeWork',
    data() {
        return {
            items: [
                'https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/case-study-gallery-3-1.jpg',
                'https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/case-study-gallery-2.jpg',
                'https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/case-study-gallery-1-1.jpg',
                'https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/11/case-study-gallery-4-1.jpg',
                'https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/11/case-study-gallery-5-1.jpg',
                'https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/11/case-study-gallery-6-1.jpg'
            ],
            index: null
        }
    }
}
</script>
<style>
    .work {
        padding-top: 100px;
        margin-top: 0;
        padding-right: 30px;
        padding-bottom: 80px;
        margin-bottom: 0px;
        padding-left: 30px;
    }
    .work .intro-text {
        padding: 3% 15% !important;
    }
    .work  h2 {
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
    .work p {
        font-size: 20px;
        font-weight: 400;
        line-height: 36px;
        margin-bottom: 20px;
        text-align: center;
    }
    .work .image {
        height: 295px;
        background-size: cover;
        position: relative;
    }
    
    .work .image .rollover {
        transform: scaleY(0);
        background-image: linear-gradient(to top, rgb(232, 234, 240) 0px, rgb(96, 122, 254) 100%);
        opacity: 0;
        display: flex;
        display: flex;
        align-items: center;
        justify-content: space-around;
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
        line-height: normal;
        text-align: center;
        transition: all .3s ease-in-out;
        -webkit-transform-style: preserve-3d;
    }
    .work .image:hover .rollover {
        transform: scaleY(1);
        opacity: 1;
    }
    .work .image .rollover-content {
        padding: 10px;
        width: 90%;
        box-sizing: border-box;
        line-height: normal;
        text-align: center;
    }
    
    .work .image .rollover-content .rollover-link {
        color: rgb(255, 255, 255);
        font-size: 30px;
    }
    .work .image .rollover-content h4 a {
        font-size: 18px;
        line-height: 1.52;
        color: rgb(255, 255, 255);
        text-decoration: none;
    }
    .work .image .rollover-content p a {
        font-size: 12px;
        line-height: 1.52;
        color: rgb(255, 255, 255);
        text-decoration: none;
    }

    .work .btn {
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
        min-width: 200px;
        text-transform: uppercase;
    }


</style>