<template>
    <div class="featured">
        <div class="row mx-0 justify-content-center">
            <h2 class="col-md-6">
                meet the new agency SEO template from the avada team
            </h2>
        </div>
        <div class="row justify-content-center">
            <p class="col-md-6">
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.
            </p>
        </div>
        <div class="row mx-0 items">
            <div class="col-md-6 col-lg-6 col-xl-4">
                <div class="item">
                    <div class="heading">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-road" />
                        </div>
                        <h3>Establish Goals</h3>
                    </div>
                    <p>
                        Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis mi ligula euismod odio vel dictum mi risus a mi.
                    </p>

                </div>

            </div>
            <div class="col-md-6 col-lg-6 col-xl-4">
                <div class="item">
                    <div class="heading">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-video" />
                        </div>
                        <h3>Work With a Team</h3>
                    </div>
                    <p>
                        Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis mi ligula euismod odio vel dictum mi risus a mi.
                    </p>

                </div>

            </div>
            <div class="col-md-6 col-lg-6 col-xl-4">
                <div class="item">
                    <div class="heading">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-droplet" />
                        </div>
                        <h3>Get Results</h3>
                    </div>
                    <p>
                        Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis mi ligula euismod odio vel dictum mi risus a mi.
                    </p>

                </div>

            </div>

        </div>
        <div class="row mx-0">
            <div class="col-12">
                <img src="https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2018/06/agency-seo-desk-front.jpg" class="img-fluid" alt="">
            </div>
        </div>
    </div>
</template>

<script>
import "animate.css/animate.min.css";
export default {
    name: 'AppHomeFeatured',
    data() {
        return {

        }
    }
}
</script>
<style>
    .featured {
        background-color: rgb(247, 248, 249);
        margin-top: 0px;
        padding-bottom: 0px;
        padding-left: 30px;
        padding-right: 30px;
        padding-top: 100px
        
    }
    .featured h2 {
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
    .featured p {
        font-size: 20px;
        font-weight: 400;
        line-height: 36px;
        margin-bottom: 20px;
        text-align: center;
    }
    .featured .items {
        margin-top: 60px
    }
    .featured .items .item{
        background-color: rgb(255, 255, 255);
        padding-bottom: 35px;
        padding-left: 35px;
        padding-right: 35px;
        padding-top: 35px;
        margin-top: 15px;
        margin-bottom: 15px;
    }
    .featured .items .item .heading{
        margin-bottom: 15px;
    }
    .featured .items .item .icon{
        margin-bottom: 15px;
    }
    .featured .items .item .icon svg{
        font-size: 36px;
        color: rgb(255, 167, 55);
        margin: 0 auto;
        display: block;
    }
    .featured .items .item h3{
        font-size: 28px;
        font-weight: 700;
        text-align: center;
        letter-spacing: -0.56px;
        line-height: 39.2px;
    }
    .featured .items .item p{
        font-size: 18px;
        font-weight: 400;
        text-align: center;
        letter-spacing: -0.27px;
        line-height: 32px;
        margin-bottom: 20px;
    }
    .featured .items .item:hover svg{
        animation: fadeInLeft 0.3s linear ;
    }
    .featured .items .item:hover h3{
        color: rgb(255, 167, 55);
    }
    @-webkit-keyframes fadeInLeft {
  from {
    opacity: 0;
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }

  to {
    opacity: 1;
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}
    
</style>