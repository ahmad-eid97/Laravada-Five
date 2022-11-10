<template>
    <section class="plans">
        <div class="row mx-0 justify-content-center">
            <h2 class="col-md-6">
                Our Plans
            </h2>
        </div>
        <div class="row justify-content-center">
            <p class="col-md-6">
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.
            </p>
        </div>
        <div class="row">
            <div class="col-md-6 col-lg-6 col-xl-3">
                <div class="plan">
                    <div class="panel">
                        <div class="panel-heading">
                            <h3>Standard</h3>
                        </div>
                        <div class="pricing-row">
                            <div class="price">
                                <span class="currency">$</span>
                                <span class="integer-part">19</span>
                                <sup class="decimal-part">99</sup>
                                <span class="time">monthly</span>
                            </div>
                        </div>
                        <ul class="list-group">
                            <li class="list-group-item">
                                5 Projects
                            </li>
                            <li class="list-group-item">
                                5 GB Storage
                            </li>
                            <li class="list-group-item">
                                Unlimited Users
                            </li>
                        </ul>
                        <div class="panel-footer">
                            <a href="#" class="btn-flat">
                                Start today
                            </a>
                        </div>
                    </div>

                </div>
            </div>
            <div class="col-md-6 col-lg-6 col-xl-3">
                <div class="plan">
                    <div class="panel">
                        <div class="panel-heading">
                            <h3>Premium</h3>
                        </div>
                        <div class="pricing-row">
                            <div class="price">
                                <span class="currency">$</span>
                                <span class="integer-part">29</span>
                                <sup class="decimal-part">99</sup>
                                <span class="time">monthly</span>
                            </div>
                        </div>
                        <ul class="list-group">
                            <li class="list-group-item">
                                10 Projects
                            </li>
                            <li class="list-group-item">
                                15 GB Storage
                            </li>
                            <li class="list-group-item">
                                Unlimited Users
                            </li>
                        </ul>
                        <div class="panel-footer">
                            <a href="#" class="btn-flat">
                                Start today
                            </a>
                        </div>
                    </div>

                </div>
            </div>
            <div class="col-md-6 col-lg-6 col-xl-3">
                <div class="plan">
                    <div class="panel">
                        <div class="panel-heading">
                            <h3>Professional</h3>
                        </div>
                        <div class="pricing-row">
                            <div class="price">
                                <span class="currency">$</span>
                                <span class="integer-part">39</span>
                                <sup class="decimal-part">99</sup>
                                <span class="time">monthly</span>
                            </div>
                        </div>
                        <ul class="list-group">
                            <li class="list-group-item">
                                15 Projects
                            </li>
                            <li class="list-group-item">
                                30 GB Storage
                            </li>
                            <li class="list-group-item">
                                Unlimited Users
                            </li>
                        </ul>
                        <div class="panel-footer">
                            <a href="#" class="btn">
                                Start today
                            </a>
                        </div>
                    </div>

                </div>
            </div>
            <div class="col-md-6 col-lg-6 col-xl-3">
                <div class="plan">
                    <div class="panel">
                        <div class="panel-heading">
                            <h3>Extreme</h3>
                        </div>
                        <div class="pricing-row">
                            <div class="price">
                                <span class="currency">$</span>
                                <span class="integer-part">59</span>
                                <sup class="decimal-part">99</sup>
                                <span class="time">monthly</span>
                            </div>
                        </div>
                        <ul class="list-group">
                            <li class="list-group-item">
                                Unlimited Projects
                            </li>
                            <li class="list-group-item">
                                Unlimited Storage
                            </li>
                            <li class="list-group-item">
                                Unlimited Users
                            </li>
                        </ul>
                        <div class="panel-footer">
                            <a href="#" class="btn-flat">
                                Start today
                            </a>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeWork',
    data() {
        return {
            
        }
    }
}
</script>
<style>
    .plans {
        padding-top: 100px;
        margin-top: 0;
        padding-right: 30px;
        padding-bottom: 80px;
        margin-bottom: 0px;
        padding-left: 30px;
        background-color: rgba(255, 255, 255, 0);
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        background-image: url("https://avada.theme-fusion.com/seo/wp-content/uploads/sites/99/2017/10/background1.jpg");
    }
    .plans  h2 {
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
        color: #fff;
    }
    .plans p {
        font-size: 20px;
        font-weight: 400;
        line-height: 36px;
        margin-bottom: 60px;
        text-align: center;
        color: #fff;
    }

    .plan {
        padding: 9px;
        box-shadow: 0 0 6px 6px rgba(0, 0, 0, 0.08);
        background-color: #F8F8F8;
        margin-bottom: 10px;
    }

    .plan .panel {
        overflow: hidden;
        margin: 0;
        background-color: #fff;
        box-shadow: none;
        border-radius: 0;
        background-clip: padding-box;
        border: 1px solid #fff;
        border-right: 1px solid #E5E4E3;
    }
    .plan .panel-heading {
        padding: 20px;
        background-clip: padding-box;
        border-bottom: 1px solid #e5e4e3;
        text-align: center;

    }

    .plan .panel-heading h3 {
        font-size: 28px;
        color: rgb(96, 122, 254);
        font-weight: 700;
        letter-spacing: -0.56px;
        line-height: 39.2px
    }

    .plan .pricing-row {
        padding: 15px;
        background-color: #f8f8f8;
        text-align: center;
    }
    .plan .pricing-row .price{
        position: relative;
    }
    .plan .pricing-row .currency{
        position: relative;
        color: #505050;
        top: -20px;
        font-size: 21px;
    }
    .plan .pricing-row .integer-part{
        font-weight: 700;
        font-size: 55px;
        color: rgb(96, 122, 254);
        letter-spacing: -0.36px;
        line-height: normal;
    }
    .plan .pricing-row .decimal-part{
        font-weight: 700;
        font-size: 17px;
        color: rgb(96, 122, 254);
        letter-spacing: -0.36px;
        line-height: 23.8px;
        top: -20px;
        position: relative;
    }
    .plan .pricing-row .time{
        color: rgb(136, 136, 136);
        font-size: 11px;
        font-style: italic;
        font-weight: 700;
        letter-spacing: -0.36px;
        line-height: 15.4px;
        margin-left: -14px;
        position: relative;
        text-align: center;
    }
    .plan .list-group .list-group-item{
        display: block;
        position: relative;
        padding: 15px;
        margin: 0;
        background: 0 0;
        border-radius: 0;
        border: 1px solid #fff;
        text-align: center;
        color: rgb(93, 95, 100);
        font-size: 18px;
        font-weight: 400;
        letter-spacing: 0.27px;
        line-height: 32.4px
    }
    .plan .panel-footer{
        padding: 20px;
        background-color: #f8f8f8;
        text-align: center;
    }

    .plan .panel-footer .btn-flat{
        border-radius: 25px 25px 25px 25px;
        background: rgba(255,255,255,0);
        border: 2px solid #fff;
        padding: 13px 29px;
        font-weight: 700;
        justify-content: center;
        letter-spacing: 0.21px;
        line-height: 17px;
        font-size: 14px;
        text-decoration: none;
        color: rgb(93, 95, 100);
        text-transform: uppercase;
        display: inline-block;
    }
    .plan .panel-footer .btn-flat:hover{
        border: 2px solid #607afa;
        color: #607afa;
    }

    .plans .btn {
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