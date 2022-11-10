<template>
    <header>
        <b-navbar toggleable="lg">
            <b-navbar-brand href="#">
                <img src="/assets/images/logo.png" alt="logoImage">
            </b-navbar-brand>

            <b-navbar-toggle target="navbar-toggle-collapse">
                <template #default="{ expanded }">
                    <span class="menu-trigger" :class="expanded ? 'active' : ''" id="menu03">
                        <span></span>
                        <span></span>
                        <span></span>
                    </span>
                </template>
            </b-navbar-toggle>

            <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-between" is-nav>
                <b-navbar-nav class="align-items-center">
                    <b-nav-item :to="localePath('/')" active-class="active" exact>Who We Are</b-nav-item>
                    <b-nav-item :to="localePath('/about')" active-class="active">What We Do</b-nav-item>
                    <b-nav-item :to="localePath('/testimonials')" active-class="active">Where We Work</b-nav-item>
                    <b-nav-item :to="localePath('/services')" active-class="active">Careers</b-nav-item>
                    <b-nav-item :to="localePath('/blogs')" active-class="active">News</b-nav-item>
                </b-navbar-nav>
                <div class="d-flex align-items-center">
                    <a href="#" class="btn">Get in touch now</a>
                    <langSwitch></langSwitch>
                </div>
            </b-collapse>
        </b-navbar>
    </header>
</template>

<script>
import langSwitch from '../langSwitch/langSwitch.vue'
// import DropdownMenu from '@innologica/vue-dropdown-menu'
export default {
    name: 'AppHeader',
    components: {
        langSwitch
        // DropdownMenu
    },
    data() {
        return {
            show: false,
            show1: false,
            topOfPage: true
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted() {
    },
    methods: {
        handleScroll(){
            if(window.pageYOffset>200){
                if(this.topOfPage) this.topOfPage = false
            } else {
                if(!this.topOfPage) this.topOfPage = true
        }
        }
    }
}
</script>
<style lang="scss">
    header {
        padding-top: 12px;
        margin-top: 0px;
        padding-right: 30px;
        padding-bottom: 12px;
        margin-bottom: 0px;
        padding-left: 30px;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 999;
        /* background: transparent !important; */
        /* position: absolute;
        left: 0;
        right: 0; */
        background: var(--main-background);
    }
    .navbar-brand {
        padding-top: 0px !important;
        padding-right: 0px !important;
        margin-right: 25px;
        padding-bottom: 0px !important;
        padding-left: 0px !important;
    }
    .navbar-brand img {
        max-width: 162px;
        height: auto;
    }
    .nav-item {
        position: relative;
        margin-right: 16px;
        justify-content: center;
        transition: all calc(300 * 1ms) cubic-bezier(.42, .01, .58, 1);
        font-size: 16px;
    }
    .navbar-nav .nav-link.active {
        color: rgb(255, 167, 55);
    }
    .nav-link {
        font-weight: 400;
        font-size: 16px;
        line-height: 29px;
        color: #fff;
    }
    .active .nav-link,.nav-link:hover {
        color: rgb(255, 167, 55);
    }
    
    .navbar-toggler,
    .navbar-toggler:focus {
        border: none;
        box-shadow: none;
    }
    .menu-trigger,
    .menu-trigger span {
    display: inline-block;
    transition: all .4s;
    box-sizing: border-box;
    }
    .menu-trigger {
    position: relative;
    width: 32px;
    height: 25px;
    background: none;
    border: none;
    appearance: none;
    cursor: pointer;
    }
    .menu-trigger span {
    position: absolute;
    left: 0;
    width: 100%;
    height: 5px;
    background-color:#fff;
    border-radius: 4px;
    }
    .menu-trigger span:nth-of-type(1) {
    top: 0;
    }
    .menu-trigger span:nth-of-type(2) {
    top: 10px;
    }
    .menu-trigger span:nth-of-type(3) {
    bottom: 0;
    }
    #menu03.active {
    transform: rotate(360deg);
    }
    #menu03.active span:nth-of-type(1) {
    transform: translateY(10px) rotate(-45deg);
    }
    #menu03.active span:nth-of-type(2) {
    transform: translateY(0) rotate(45deg);
    }
    #menu03.active span:nth-of-type(3) {
    opacity: 0;
    }

    nav .btn {
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

    nav .btn:hover {
        color: rgb(255, 255, 255);
        border-color: #fff;
    }

    @include md {
        nav .btn {
            display: none;
        }
    }
    
    @media screen and (max-width: 991px) {
        .navbar-collapse.show .navbar-nav {
            position: absolute;
            width: 250px;
            top: 56px;
            right: 0;
        }
        .nav-item {
            width: 100%;
            border-bottom: 1px solid #e5e5e5;
            background: #fff;
        }
        .nav-item .nav-link {
            color: #000;
        }
        .nav-item:after {
            content: none;
        }
        .nav-item.active ,
        .nav-item:hover {
            background-color:rgb(255, 167, 55);;
        }
        .nav-item.active .nav-link ,
        .nav-item:hover .nav-link {
            color: #fff;
        }
        .nav-link {
            padding: 8px 20px !important;
            font-weight: 800;
            font-size: 15px;
            text-align: right;
        }
    }
</style>