<template>
<nav>
    <div class="navigation">
        <div class="nav-bar">
            <div class="left-bar">
                <div class="logo-center">
                    <div class="logo">
                        <img src="/logo.png" alt="" class="img-logo">
                        <div class="text-logo">
                            <h1><RouterLink class="text-logo-h1" to="/">Eatly</RouterLink></h1>
                        </div>
                    </div>
                </div>
                <div class="nav2-center">
                    <div class="nav2">
                        <h1 v-for="(navigation, index) in navigations" :key="index" class="text-nav2"><RouterLink :to="navigation.route" class="router">{{navigation.text}}</RouterLink></h1>
                    </div>
                </div>
            </div>
            <div class="right-bar">
                <div class="buttons-nav">
                    <button v-for="(navbutton, index) in navbuttons" :key="index" class="nav-button" :style="{width: navbutton.width}"><h1 class="navbtn-text">{{navbutton.text}}</h1></button>
                </div>
            </div>
        </div>
        <div class="nav-line-overflow">
            <div class="nav-line">
            </div>
        </div>
        <div class="nav-bar-mobile-column">
            <div class="nav-bar-mobile">
                <div class="logo-center">
                    <div class="logo">
                        <img src="/logo.png" alt="" class="img-logo">
                        <div class="text-logo">
                            <h1><RouterLink class="text-logo-h1" to="/">Eatly</RouterLink></h1>
                        </div>
                    </div>
                </div>
                <Slide :isOpen="isOpen" @closeMenu="isOpen = false" noOverlay width="200">
                    <img src="/logo.png" />
                    <h1 v-for="(navigation, index) in navigations" :key="index"><router-link :to="navigation.route" class="mob">{{navigation.text}}</router-link></h1>
                </Slide>
            </div>
            <div class="nav-line-overflow-mob">
                <div class="nav-line-mob">
                </div>
            </div>
        </div>
        
    </div>
</nav>
</template>
<script>
import { Slide } from 'vue3-burger-menu';
export default {
    components: { Slide },
    data () { 
        return {
            navigations: [
                {
                    text: 'Menu',
                    route: '/menu'
                },
                {
                    text: 'Blog',
                    route: '/blog'
                },
                {
                    text: 'Pricing',
                    route: '/pricing'
                },
                {
                    text: 'Contact',
                    route: '/contact'
                },

            ],
            navbuttons: [
                {   
                    width: '102.49px',
                    text: 'Login',
                },
                {
                    width: '131.49px',
                    text: 'Sign Up',
                },
            ]
        }
    }
}
</script>

<style>
.logo-center {
    height: 62.66px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: relative;
    top: -2px;
    padding-left: 31px;
    padding-top: 22.5px;
}
.text-logo-h1 {
    font-weight: 600;
    font-size: 21px;
    color: #6C5FBC;
    text-decoration: none;
}
.img-logo {
    width: 45.94px;
    height: 42.31px;
    position: relative;
    top: 2px;
}
.logo {
    width: 112px;
    height: 42.31px;
    display: flex;
    flex-direction: row;
    justify-content: center;
}
.text-logo {
    height: 42.31px;
    margin-left: 15px;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.nav-bar-mobile {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
.nav-bar-mobile-column {
    display: block;
    height: 150px;
}
.nav-bar {
    display: none;
}
div.bm-burger-button {
    position: relative;
    width: 36px;
    height: 30px;
    left: auto;
    right: 25px;
    top: 36px;
    cursor: pointer;
}
.mob {
    text-decoration: none;
    color: #6C5FBC;
    font-family: "Poppins", sans-serif;
    width: 300px;
}

div.bm-burger-bars {
    background-color: #373a47;
}
.bm-burger-bars.line-style {
    position: absolute;
    height: 2px;
    border-radius: 2px;
    left: 0;
    right: 0;
}
div.cross-style {
    position: absolute;
    top: 12px;
    right: 2px;
    cursor: pointer;
}
div.bm-cross {
    background: #bdc3c7;
}
.bm-cross-button {
    height: 24px;
    width: 24px;
    padding-right: 25px;
    padding-top: 25px;
}
div.bm-menu {
    height: 100%; 
    width: 0; 
    position: fixed; 
    z-index: 1000; 
    top: 0;
    box-shadow: 15px 15px 345px 0.1px black;
    left: 0;
    background-color: rgb(255, 255, 255); 
    overflow-x: hidden; 
    padding-top: 60px; 
    transition: 0.5s; 
}

div.bm-overlay {
    background: rgba(0, 0, 0, 0.3);
}
.bm-item-list {
    color: #b8b7ad;
    position: relative;
    top: -40px;
    margin-left: 10%;
    font-size: 20px;
    width: 300px;
}
div.bm-item-list > * {
    display: flex;
    text-decoration: none;
    padding: 0.7em;
}
div.bm-item-list > * > span {
    margin-left: 10px;
    font-weight: 700;
    color: white;
}
.nav-line-overflow {
    display: none;
}
.nav-line-overflow-mob {
    display: flex;
    justify-content: center;
    padding-left: 25px;
    padding-right: 25px;
}
.nav-line-mob {
    width: 100%;
    min-width: 100px;
    height: 0.5px;
    top: 25px;
    background-color: #CBCBCB;
    left: 1px;
    gap: 0px;
    padding-left: 96px;
    padding-right: 96px;
    border: 1px 0px 0px 0px;
    position: relative;


}
@media (min-width:641px)  {
    .nav-line-overflow {
        display: none;
    }
    .nav-line-overflow-mob {
        display: flex;
        justify-content: center;
        padding-left: 25px;
        padding-right: 25px;
    }
    .nav-bar-mobile-column {
        display: block;
        height: 150px;
    }
    .logo-center {
        height: 62.66px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        position: relative;
        top: -2px;
        padding-left: 31px;
        padding-top: 22.5px;
    }
    .text-logo-h1 {
        font-weight: 600;
        font-size: 21px;
        color: #6C5FBC;
        text-decoration: none;
    }
    .img-logo {
        width: 45.94px;
        height: 42.31px;
        position: relative;
        top: 2px;
    }
    .logo {
        width: 112px;
        height: 42.31px;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
    .text-logo {
        height: 42.31px;
        margin-left: 15px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .nav-bar-mobile {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .nav-bar {
        display: none;
    }
    div.bm-burger-button {
        position: relative;
        width: 36px;
        height: 30px;
        left: auto;
        right: 25px;
        top: 36px;
        cursor: pointer;
    }
    .mob {
        text-decoration: none;
        color: #6C5FBC;
        font-family: "Poppins", sans-serif;
        width: 300px;
    }
    
    div.bm-burger-bars {
        background-color: #373a47;
    }
    div.line-style {
        position: absolute;
        height: 20%;
        left: 0;
        right: 0;
    }
    div.cross-style {
        position: absolute;
        top: 12px;
        right: 2px;
        cursor: pointer;
    }
    div.bm-cross {
        background: #bdc3c7;
    }
    .bm-cross-button {
        height: 24px;
        width: 24px;
        padding-right: 25px;
        padding-top: 25px;
    }
    div.bm-menu {
        height: 100%; 
        width: 0; 
        max-width: 352px;
        position: fixed; 
        top: 0;
        left: 0;
        background-color: rgb(255, 255, 255); 
        overflow-x: hidden; 
        padding-top: 60px; 
        transition: 0.5s; 
    }
  
    div.bm-overlay {
        background: rgba(0, 0, 0, 0.3);
    }
    .bm-item-list {
        color: #b8b7ad;
        position: relative;
        top: -40px;
        margin-left: 10%;
        font-size: 20px;
        width: 300px;
    }
    div.bm-item-list > * {
        display: flex;
        text-decoration: none;
        padding: 0.7em;
    }
    div.bm-item-list > * > span {
        margin-left: 10px;
        font-weight: 700;
        color: white;
    }
    .nav-line-mob {
        width: 100%;
        min-width: 100px;
        height: 0.5px;
        top: 25px;
        background-color: #CBCBCB;
        left: 1px;
        gap: 0px;
        padding-left: 96px;
        padding-right: 96px;
        border: 1px 0px 0px 0px;
        position: relative;
    
    
    }
}

@media (min-width:1086px) {
    
    .nav-bar-mobile-column {
        display: none;
    } 
    .right-bar {
        flex-direction: column;
        justify-content: center;
        top: 5px;
    } 
    .nav-line {
        width: 100%;
        min-width: 314px;
        height: 0.5px;
        top: 25px;
        background-color: #CBCBCB;
        left: 1px;
        gap: 0px;
        padding-left: 96px;
        padding-right: 96px;
        border: 1px 0px 0px 0px;
        display: flex;
        position: relative;
    
    
    }
    .router {
        text-decoration: none;
        color: #606060;
        transition: all 0.3s ease;
        background-color: transparent;
    }
    .router:hover {
        color: #6C5FBC;
        background-color: transparent;
    }
    .nav-line-mob {
        display: none;
    }
    .nav-line-overflow {
        display: flex;
        max-width: 6248px;
        min-width: 314px;
        height: 30px;
        
    }
    .navigation {
        max-width: 6248px;
        min-width: 314px;
        height: 100px;
        display: flex;
        padding-left: 96px;
        padding-right: 96px;
        padding-top: 28px;
        flex-direction: column;
        justify-content: center;
    }
    .nav-button {
        width: 152.49px;
        height: 62.66px;
        border: 0px transparent;
        cursor: pointer;
        gap: 11.14px;
        border-radius: 17.83px;
        transition: all 0.5s ease;
        color: #6C5FBC;
        background-color: white;
        border: 1.5px solid #6C5FBC;
    
    
    }
    .nav-button:active {
        scale: 0.9;
    }
    .nav-button:hover {
        background-color: #6C5FBC;
        color: white;
    }
    .navbtn-text {
        font-family: 'Inter';
        font-size: 17.83px;
        font-weight: 700;
        line-height: 26.74px;
        text-align: center;
    
    }
    .buttons-nav {
        display: flex;
        flex-direction: row;
        width: 232.89px;
        height: 62.66px;
        top: -1px;
        left: 1015.12px;
        gap: 8.91px;
    
    
    }
    .text-logo-h1 {
        font-weight: 600;
        font-size: 21.18px;
        color: #6C5FBC;
        text-decoration: none;
    }
    .img-logo {
        width: 46px;
        height: 42.31px;
        position: relative;
        top: 7px;
    }
    .logo {
        width: 112px;
        height: 42.31px;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
    .text-logo {
        height: 42.31px;
        margin-left: 15px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        position: relative;
        top: 7px;
    }
    .nav-bar {
        max-width: 6248px;
        min-width: 314px;
        height: 62.4px;
        padding: 0px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .nav2-center {
        height: 42.3px;
        width: 374.46px;
        display: flex;
        flex-direction: column;
        justify-content: end;
    }
    .logo-center {
        height: 62.66px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        position: relative;
        padding: 0px;
        top: -5px;
    }
    .nav2 {
        margin-left: 103.06px;
        width: 374.46px;
        height: 27px;
        display: flex;
        flex-direction: row;
        position: relative;
        background-color: transparent;
        top: 5px;
    }
    .text-nav2 {
        font-family: 'Inter';
        font-size: 17.83px;
        font-weight: 500;
        color: #606060;
        line-height: 26.74px;
        text-align: left;
        margin-right: 40px;
        background-color: transparent;
        transition: all 0.5s ease;
    
    }
    .text-nav2:hover {
        translate: 0px -5px;
    }
    .left-bar {
        display: flex;
        flex-direction: row;
    }
}

</style>