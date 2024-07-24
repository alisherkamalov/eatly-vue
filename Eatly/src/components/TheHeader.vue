
<template>
    <header>
        <div class="hero-container">
            <div class="hero-text">
                <div class="line-and-herotext">
                    <div class="line"></div>
                    <h1 class="hero-textover">OVER 1000 USERS</h1>
                </div>
                <h1 :class="herotext.class" v-for="(herotext,index) in herotexts" :key="index" >
                    {{ herotext.text }}<span :class="herotext.classspan">{{ herotext.span }}</span>
                </h1>
                <h1 :class="herotextmob.class" v-for="(herotextmob,index) in herotextsmob" :key="index" >
                    {{ herotextmob.text }}<span :class="herotextmob.classspan">{{ herotextmob.span }}</span>
                </h1>
                <div class="herobuttons">
                    <button class="hero-button" v-for="(herobutton,index) in herobuttons" :key="index"
                    :style="{
                        backgroundColor: herobutton.bgcolor,
                        color: herobutton.color,
                        border: herobutton.border,
                        width: herobutton.width
                    }"
                    >
                        {{ herobutton.text }}
                    </button>
                </div>
                <div class="trust-reviews">
                    <div 
                    class="trust-review" 
                    v-for="(trust,index) in trusts" :key="index"
                    :style="{
                        width: trust.width,
                        height: trust.height,
                        marginLeft: '15px',
                        marginTop: trust.mt
                    }"
                    >
                        <img :src="trust.image" alt="images trust">
                    </div>
                    <h1 class="h1-trust">4900+</h1>
                </div>
                
            </div>
            <div class="hero-img">
                <img src="/hero.png" alt="" class="hero-image">
            </div>
        </div>
    </header>
</template>
<script>
export default {
    data () {
        return {
            herotexts: [
                {
                    text: 'Enjoy Foods All Over The ',
                    span: 'World',
                    class: 'herotext1',
                    classspan: 'herotextspan1'
                    

                },
                {
                    text: 'EatLy help you set saving goals, earn cash back offers, Go to disclaimer for more details and get paychecks up to two days early. Get a ',
                    span: '$20 bonus.',
                    class: 'herotext2',
                    classspan: 'herotextspan2'

                }

            ],
            herotextsmob: [
                {
                    text: 'Enjoy Foods Over ',
                    span: 'World',
                    class: 'herotext1mob',
                    classspan: 'herotextspan1mob'
                    

                },
                {
                    text: 'EatLy help you set saving goals, earn cash back offers, Go to disclaimer for more details and get paychecks up to two days early. Get a ',
                    span: '$20 bonus.',
                    class: 'herotext2mob',
                    classspan: 'herotextspan2mob'

                }

            ],
            herobuttons: [
                { 
                    text: 'Get Started' ,
                    bgcolor: '#6C5FBC',
                    color: 'white',
                    border: '0px solid transparent',
                    width: '156px'
                },
                { 
                    text: 'Go Pro',
                    bgcolor: 'white',
                    color: '#6C5FBC',
                    border: '1.5px solid #6C5FBC',
                    width: '110px'
                }
            ],
            trusts: [
                {
                    width: '123px',
                    height: '30.2px',
                    mt: '0px',
                    image: '/trust.png'
                },
                {   
                    width: '95.79px',
                    height: '15.28px',
                    mt: '6px',
                    image: '/stars.png'
                },
                
            ]
        }
    }
}
</script>
<style>
.trust-reviews {
    display: flex;
    width: 301px;
    height: 31px;
    justify-content: center;
    align-items: center;
    top: 35px;
    position: relative;
    margin-bottom: 25px;
}
.h1-trust {
    margin-top: 10px;
    margin-left: 10px;
    color: #334155;
    font-size: 16px;
    font-weight: 500;


}
.hero-button {
    width: 156px;
    height: 59px;
    font-family: 'Poppins';
    border-radius: 15.41px;
    cursor: pointer;
    margin-right: 15px;
    transition: all 0.5s ease;


}
.hero-button:active {
    scale: 0.9;
}
.hero-container {
    width: 100%;
    height: 700px;
    justify-content: center;
    flex-wrap: wrap;
    display: flex;
    flex-direction: row;
    left: 26px;
}
.hero-texts {
    font-family: 'Poppins';
    font-size: 35px;
    width: 600px;

}
.hero-texts span {
    color: #6C5FBC;
}
.hero-text {
    width: 568px;
    height: 492px;
    justify-content: center;
    display:flex;
    flex-direction: column;
    align-items: center;

}
.hero-img {
    width: 332.92px;
    height: 288.14px;
    position: relative;
}
.hero-image {
    width: 332.92px;
    height: 288.14px;
    position: relative;
    margin-top: 60px;
}
.line-and-herotext {
    display: flex;
    width: 231px;
    height: 18px;
}
.line {
    width: 54px;
    height: 0.5px;
    margin-top: 7.5px;
    margin-right: 15px;
    background-color: #201F1F33;
}
.hero-textover {
    color: #201F1F33;
    font-family: "Poppins";
    font-size: 15px;
    font-weight: 600;
    line-height: 18px;
    letter-spacing: 2px;
    text-align: center;


}
@media (max-width:640px) {
    .hero-container {
        width: 100%;
        height: 600px;
        justify-content: center;
        flex-wrap: wrap;
        display: flex;
        flex-direction: row;
        left: 26px;
    }
    .hero-texts {
        font-family: 'Poppins';
        font-size: 35px;
        width: 600px;
    
    }
    .hero-texts span {
        color: #6C5FBC;
    }
    .hero-text {
        width: 332.92px;
        height: 305px;
        padding-top: 50px;
        justify-content: center;
        display:flex;
        flex-direction: column;
        align-items: center;
    
    }
    .herotext1 {
        display: none;
    }
    .herotext2 {
        display: none;
    }
    h1.herotext1mob {
        font-family: 'Poppins';
        font-size: 46.24px;
        font-weight: 600;
        line-height: 55.49px;
        letter-spacing: -1.8495762348175049px;
        text-align: center;

        
    }
    h1.herotext2mob {
        font-family: 'Inter';
        font-size: 11.1px;
        font-weight: 400;
        line-height: 17.26px;
        text-align: center;
        margin-top: 15px;
        color: #676767;
        margin-bottom: 25px;
        

    }
    .herotextspan1mob {
        font-weight: 600;
        color: #6C5FBC;
        font-family: 'Poppins';
        font-size: 46.24px;
    }
    .herotextspan2mob {
        font-weight: 500;
        color: #6C5FBC;
    }
    
    .hero-img {
        width: 332.92px;
        height: 298.14px;
        
        position: relative;
    }
    .hero-image {
        width: 332.92px;
        height: 298.14px;
        position: absolute;
    }
    .line-and-herotext {
        display: flex;
        width: 202.62px;
        height: 21px;
        margin-bottom: 25px;
    }
    .line {
        width: 54px;
        height: 0.5px;
        margin-top: 8px;
        margin-right: 1px;
        background-color: #201F1F33;
    }
    .hero-textover {
        color: black;
        font-size: 9.25px;
        font-weight: 600;
        width: 157px;
        height: 11px;



    
    }
}
@media (min-width:641px)  {
    .herotext1mob {
        display: none;
    }
    .herotext2mob {
        display: none;
    }
    .hero-container {
        width: 100%;
        height: 25%;
        justify-content: center;
        flex-wrap: wrap;
        display: flex;
        flex-direction: row;
        left: 26px;
        overflow: hidden;
    }
    h1.herotext1 {
        font-size: 53.33px;
        font-family: 'Poppins';
        font-weight: 600;
        width: 500px;
        color: 'black';
    }
    h1.herotext2 {
        font-family: 'Inter';
        width: 360px;
        font-size: 12.8px;
        font-weight: 400;
        color: #676767;
        margin-bottom: 50px;

    }
    .herotextspan1 {
        font-weight: 600;
        color: #6C5FBC;
    }
    .herotextspan2 {
        font-weight: 500;
        color: #6C5FBC;
    }
    
    .hero-text {
        width: 403.2px;
        height: 350.38px;
        justify-content: center;
        display: block;
    }
    .hero-img {
        width: 483.9px;
        height: 431.65px;
    }
    .hero-image {
        width: 483.9px;
        height: 431.65px;
        margin-top: 0px;
    }
    .line-and-herotext {
        display: flex;
        width: 211px;
        height: 13px;

    }
    .line {
        width: 38.4px;
    }
    .hero-textover {
        font-size: 10.67px;
        font-weight: 600;



    }
}

@media (min-width:1086px) {
    .herotext1mob {
        display: none;
    }
    .herotext2mob {
        display: none;
    }
    h1.herotext1 {
        font-size: 65px;
        font-family: 'Poppins';
        font-weight: 600;
        width: 550px;
        color: 'black';
    }
    h1.herotext2 {
        font-family: 'Inter';
        width: 500px;
        font-size: 18px;
        font-weight: 400;
        margin-bottom: 50px;
        color: #676767;
        

    }
    .herotextspan1 {
        font-weight: 600;
        color: #6C5FBC;
    }
    .herotextspan2 {
        font-weight: 500;
        color: #6C5FBC;
    }
    
    .line-and-herotext {
        display: flex;
        width: 231px;
        height: 18px;
    }
    .line {
        width: 54px;
        height: 0.5px;
        margin-top: 7.5px;
        margin-right: 15px;
        background-color: #201F1F33;
    }
    .hero-textover {
        color: #201F1F33;
        font-family: "Poppins";
        font-size: 15px;
        font-weight: 600;
        line-height: 18px;
        letter-spacing: 2px;
        text-align: center;


    }
    .hero-container {
        width: 100%;
        height: 700px;
        justify-content: center;
        flex-wrap: nowrap;
        display: flex;
        flex-direction: row;
    }
    .hero-text {
        width: 568px;
        height: 492px;
        display: block;
        position: relative;
        margin-right: 40px;
        left: 96px;
        top: 96px;

    }
    .hero-img {
        width: 680.48px;
        height: 607px;
    }
    .hero-image {
        width: 680.48px;
        height: 607px;
        min-width: 692.92px;
        min-height: 298.14px;
        margin-top: 0px;
    }
}
</style>
