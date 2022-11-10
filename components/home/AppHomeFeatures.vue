<template>
    <section class="features">
        <div class="row align-items-center">
            <div class="col-6 p-0">
                <div class="feature-1">
                    <div class="feature-inner">
                        <h2>Financial Freedom could be just one phonecall away…</h2>
                        <div class="seprator">
                            <img src="https://avada.theme-fusion.com/financial-advisor/wp-content/uploads/sites/145/2020/08/slant-separator.png" alt="">
                        </div>
                        <p>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas magna ligula, rutrum in venenatis aliquet, congue gravida lorem. Aliquam convallis orci a odio imperdiet, nec pharetra odio porta. Aenean quis tincidunt elit. Donec feugiat, justo interdum tincidunt efficitur, tortor diam volutpat libero, sed accumsan erat mauris ac elit. Donec ultricies nisi quis leo aliquam faucibus quis et metus. Donec eget viverra arcu. Duis feugiat diam dolor, sed placerat nibh condimentum ac. Aliquam in rutrum ante.
                        </p>
                    </div>
                    <div class="feature-shape">
                        <div class="row mx-0">
                            <div class="col image p-0">
                                <img src="https://avada.theme-fusion.com/financial-advisor/wp-content/uploads/sites/145/2020/08/testimonial-image.jpg" alt="">
                            </div>
                            <div class="col text p-0">
                                <div class="text-inner">
                                    <h2>Phenomenal</h2>
                                    <p>
                                        <em>
                                            Going from clueless with money to being savvy enough to invest in my future and live well within my means in what feels like an instant after talking to Avada Financial Consultants has really put my mind at rest and I can now make informed,educated smart decisions with my money.
                                        </em>
                                    </p>
                                    <p>
                                        <a href="#">
                                            <strong>Read More Testimonials</strong>
                                        </a>
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-6 p-0">
                <div class="feature-2">
                    <div class="feature-inner">
                        <h2>Financial Freedom could be just one phonecall away…</h2>
                        <div class="seprator">
                            <img src="https://avada.theme-fusion.com/financial-advisor/wp-content/uploads/sites/145/2020/08/slant-separator.png" alt="">
                        </div>
                        <p>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas magna ligula, rutrum in venenatis aliquet, congue gravida lorem. Aliquam convallis orci a odio imperdiet, nec pharetra odio porta.
                        </p>
                        <div class="accordion-container">
                            <b-card-header header-tag="div" class="p-1" role="tab">
                                <div v-b-toggle.accordion-1>
                                    <font-awesome-icon icon="fa-solid fa-plus" />
                                    <font-awesome-icon icon="fa-solid fa-minus" />
                                    <span >Can We Consult Remotely?</span>
                                </div>
                            </b-card-header>
                            <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
                                <b-card-body>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus vulputate blandit egestas. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae;
                                    </p>
                                </b-card-body>
                            </b-collapse>
                        </div>
                        <div class="accordion-container">
                            <b-card-header header-tag="div" class="p-1" role="tab">
                                <div v-b-toggle.accordion-2>
                                    <font-awesome-icon icon="fa-solid fa-plus" />
                                    <font-awesome-icon icon="fa-solid fa-minus" />
                                    <span >Can We Consult Remotely?</span>
                                </div>
                            </b-card-header>
                            <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                                <b-card-body>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus vulputate blandit egestas. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae;
                                    </p>
                                </b-card-body>
                            </b-collapse>
                        </div>
                        <div class="accordion-container">
                            <b-card-header header-tag="div" class="p-1" role="tab">
                                <div v-b-toggle.accordion-3>
                                    <font-awesome-icon icon="fa-solid fa-plus" />
                                    <font-awesome-icon icon="fa-solid fa-minus" />
                                    <span >Can We Consult Remotely?</span>
                                </div>
                            </b-card-header>
                            <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
                                <b-card-body>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus vulputate blandit egestas. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae;
                                    </p>
                                </b-card-body>
                            </b-collapse>
                        </div>
                        <div class="accordion-container">
                            <b-card-header header-tag="div" class="p-1" role="tab">
                                <div v-b-toggle.accordion-4>
                                    <font-awesome-icon icon="fa-solid fa-plus" />
                                    <font-awesome-icon icon="fa-solid fa-minus" />
                                    <span >Can We Consult Remotely?</span>
                                </div>
                            </b-card-header>
                            <b-collapse id="accordion-4" accordion="my-accordion" role="tabpanel">
                                <b-card-body>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus vulputate blandit egestas. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae;
                                    </p>
                                </b-card-body>
                            </b-collapse>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeFeatures',
    data() {
        return {

        }
    }
}
</script>
<style>
    .features {
        padding-top: 70px;
        margin-top: 0px;
        padding-right: 30px;
        padding-bottom: 70px;
        margin-bottom: 0px;
        padding-left: 30px;
        background-color: rgba(255, 255, 255, 0);
        background-position: center center;
        background-repeat: no-repeat;
        border-width: 0px;
        border-style: solid;
        background-size: cover;
        background-image: url("https://avada.theme-fusion.com/financial-advisor/wp-content/uploads/sites/145/2020/08/home-content-background-scaled.jpg");
    }
    .features .feature-1 {
        margin-left: 25px;
        margin-right: 43px;
        min-height: 1px;
        padding-bottom: 0px;
        padding-left: 86px
    }
    .features .feature-2 {
        margin-left: 25px;
        margin-right: 43px;
        min-height: 1px;
        padding-bottom: 0px;
        padding-right: 170px
    }
    .features .feature-1 .feature-inner {
        padding-bottom: 0px;
        padding-left: 106px;
        padding-right: 0px;
        padding-top: 0px
    }
    .features  h2{
        color: rgb(33, 41, 52);
        font-size: 35px;
        font-weight: 800;
        letter-spacing: -1px;
        line-height: 42px;
        text-align: left;
        margin-top: 10px;
        margin-right: 0px;
        margin-bottom: 15px;
        margin-left: 0px;
    }

    .features .seprator img{
        width: 70px;
        margin-top: 5px;
        margin-bottom: 20px;
    }
    .features  .feature-inner p{
        margin-top: 0;
        margin-bottom: 20px;
        color: rgb(74, 78, 87);
        font-size: 16px;
        line-height: 29px
    }
    .features .feature-1 .feature-shape{
        margin-top: 120px
    }
    .features .feature-1 .feature-shape .image{
        margin-left: 10px;
        margin-right: 10px;
        overflow: hidden;
    }
    .features .feature-1 .feature-shape .image img{
        width: 231px;
        max-width: 100%;
        border-radius: 40px;
    }
    .features .feature-1 .feature-shape .text{
        margin-top: 100px;
        margin-bottom: -30px;
        width: 250px;
    }
    .features .feature-1 .feature-shape .text .text-inner{
        background-color: #fff;
        overflow: hidden;
        width: 250px;
        border-radius: 60px 12px 60px 12px;
        padding-top: 51px !important;
        padding-right: 36px !important;
        margin-right: 3.84%;
        padding-bottom: 33px !important;
        padding-left: 43px !important;
        margin-left: -80px;
        box-shadow: rgba(0, 0, 0, 0.12) 0px 20px 33px 0px
    }
    .features .feature-1 .feature-shape .text .text-inner p {
        font-size: 14px;
        font-weight: 700;
        line-height: 25.2px;
        color: rgb(33, 41, 52);
        text-decoration: none;
        margin-bottom: 20px;
    }
    .features .feature-1 .feature-shape .text .text-inner a {
        font-size: 14px;
        font-weight: 700;
        line-height: 25.2px;
        color: rgb(33, 41, 52);
        text-decoration: none;
        margin-top: 15px;
    }
    .collapsed .fa-minus {
        display: none;
    }
    .not-collapsed .fa-plus {
        display: none;
    }

    .accordion-container {
        border-bottom: 1px solid #e2e2e2;
                padding-bottom: 20px;
    }
    .accordion-container svg {
        color: rgb(83, 94, 229);
        font-size: 18px;
    }
    .accordion-container span {
        margin-left: 18px;
        font-weight: 800;
        font-size: 18px;
        color: rgb(33, 41, 52);
    }
    .accordion-container .card-body{
        padding: 15px 0;
        
    }
    .accordion-container .p{

        line-height: 29px;
        font-size: 16px;
    }
</style>