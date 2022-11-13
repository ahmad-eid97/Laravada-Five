<template>
    <footer>
        <div class="row justify-content-center">
            <div class="col-auto">
                <img src="/assets/images/logo2.png" alt="logoImage">
            </div>
        </div>
        <b-navbar-nav class="align-items-center justify-content-center line footerLinks">
            <nuxt-link :to="localePath('/contact')">Contact</nuxt-link>
            <nuxt-link :to="localePath('/faq')">FAQs</nuxt-link>
            <nuxt-link :to="localePath('/policy')">Privacy Policy</nuxt-link>
            <nuxt-link :to="localePath('/terms')">Terms & Conditions</nuxt-link>
        </b-navbar-nav>
        <div class="row mx-0 justify-content-center">
            <div class="col-auto copyright">
                <p>© Copyright 2023&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;Laravada Theme&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;All Rights Reserved&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;Powered by <a href="http://wordpress.org" target="_blank" rel="noreferrer">Rail Coder</a></p>
            </div>
        </div>
        <div class="row mx-0 align-items-center justify-content-center">
            <div class="col-auto social">
                <a href="#" >
                    <font-awesome-icon icon="fa-brands fa-facebook-f" />
                </a>
                <a href="#" >
                    <font-awesome-icon icon="fa-brands fa-twitter" />
                </a>
                <a href="#" >
                    <font-awesome-icon icon="fa-brands fa-youtube" />           
                </a>
                <a href="#" >
                    <font-awesome-icon icon="fa-brands fa-instagram" />          
                </a>
                <a href="#" >
                    <font-awesome-icon icon="fa-brands fa-linkedin-in" />          
                </a>
            </div>
        </div>
    </footer>
</template>

<script>


export default {
    name: 'AppFooter',
    components: {},
    data() {
        return {
            
        }
    },
    methods : {
        
    },
    mounted() {
        console.log(this.$store.state.footerLinks)
    }
}
</script>
<style lang="scss">
    footer{
        padding-top: 48px;
        margin-top: 0px;
        padding-right: 30px;
        padding-bottom: 48px;
        margin-bottom: 0px;
        padding-left: 30px;
    }

    footer img {
        margin-right: 24px;
        padding-top: 46px;
        width: 200px;
    }

    footer .navbar-nav {
        flex-direction: row;
    }
    footer .navbar-nav .nav-item{
        padding: 25px 20px;
    }
    footer .navbar-nav .nav-link{
        color: rgb(33, 41, 52);
    }
    footer .nav-link.active ,
    footer .nav-link:hover {
        color:rgb(255, 167, 55);;
    }

    footer .copyright {
        font-size: 13px;
        color: rgb(93, 95, 100);
        font-weight: 400;
        letter-spacing: 0.27px;
        line-height: 23.4px;
        
    }
    footer .copyright a{
        color: rgb(255, 167, 55);
        text-decoration: none;
    }
    footer .social a {
        color: rgb(93, 95, 100);
        cursor: pointer;
        display: inline-block;
        font-size: 20px;
        margin: 10px;
    }
    @include sm {
        .line li {
            padding-right: 0 !important;
            padding-left: 0 !important;
        }
    }
    @include xs {
        .line {
            display: block;
        }
        .line li {
            padding: 0 !important;
        }
    }
</style>