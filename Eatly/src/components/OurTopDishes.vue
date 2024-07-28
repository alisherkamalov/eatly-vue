<template>
    <div class="root-dishes">   
        <div class="dishes">
            <h1 class="dishes-text">Our Top <span class="dishes-span">Dishes</span></h1>
            <div class="foods">
                <div :class="food.class" v-for="(food,index) in foods" :key="index">
                    <img src="/heart.png" class="heart-image"/>
                    <img :src="food.image" class="food-img" 
                    :style="{
                        paddingLeft: food.padding,
                        marginBottom: food.margin
                    }"/>
                    <div class="content-food">
                        <div class="dishes-highlight"
                        :style="{
                            backgroundColor: food.highcolor
                        }">
                            <h1 class='highlight-text' 
                            :style="{
                                color: food.highcolortext
                            }">{{food.hightext}}</h1>
                        </div>
                        <div class="info-food-content">
                            <h1 class="i-f-c-text">{{food.text}}</h1>
                        </div>
                        <div class="bottom-i-f-c">
                            <div class="b-i-f-c-left">
                                <h1 class="bottom-i-f-c-t">{{food.minutes}}</h1>
                                <img src="/star-purple.png" class="star-purp"/>
                                <h1 class="bottom-i-f-c-t">{{food.rating}}</h1>
                            </div>
                            <div class="b-i-f-c-right"> 
                                <img src="/add-dishes.png"/>
                            </div>
                            <div class="price-dish">
                                <h1 class="price-dish-h1">{{food.price1}}<span class="price-dish-span">{{food.price2}}</span></h1>
                            
                            </div>
                            
                        </div>
                    </div>
        
                    
                </div>
            </div>
        </div>
    </div>
    <div class="center-b-d">
        <div class="bottom-dishes">
            <h1 class="b-d-text">View All -></h1>
        </div>
    </div>
    
    <div class="nav-line-overflow">
        <div class="nav-line"></div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            foods: [
                {
                    text:'Chicken Hell',
                    image: '/food-img1.png',
                    hightext:'Healthy',
                    highcolor:'#F7EDD0',
                    highcolortext:'#DAA31A',
                    minutes:'24min •',
                    rating:'4.8',
                    padding: '0px',
                    margin: '0px',
                    price1: '$12',
                    price2: '.99',
                    class: 'foods-cont'
                },
                {
                    text:'Swe Dish',
                    image: '/food-img3.png',
                    hightext:'Trending',
                    highcolor:'#F7C5BA',
                    highcolortext:'#FB471D',
                    minutes:'34min •',
                    rating:'4.9',
                    padding: '15px',
                    margin: '21px',
                    price1: '$19',
                    price2: '.99',
                    class: 'foods-cont'
                },
                {
                    text:'Swe Dish',
                    image: '/food-img2.png',
                    hightext:'Supreme',
                    highcolor:'#D6EEE0',
                    highcolortext:'#33AC64',
                    minutes:'34min •',
                    rating:'4.8',
                    padding: '15px',
                    margin: '21px',
                    price1: '$19',
                    price2: '.99',
                    class: 'foods-cont'
                },
                {
                    text:'Chicken Hell',
                    image: '/food-img1.png',
                    hightext:'Healthy',
                    highcolor:'#F7EDD0',
                    highcolortext:'#DAA31A',
                    minutes:'24min •',
                    rating:'4.9',
                    padding: '0px',
                    margin: '0px',
                    price1: '$12',
                    price2: '.99',
                    class: 'foods-cont4'
                },
                {
                    text:'Swe Dish',
                    image: '/food-img3.png',
                    hightext:'Trending',
                    highcolor:'#F7C5BA',
                    highcolortext:'#FB471D',
                    minutes:'34min •',
                    rating:'4.8',
                    padding: '15px',
                    margin: '21px',
                    price1: '$19',
                    price2: '.99',
                    class: 'foods-cont5'
                },


            ]
        }
    }
}
</script>

<style scoped>
.center-b-d {
    width: 100%;
    height: 150px;
    display: flex;
    justify-content: center;
    position: relative;
    top: -60px;
}
.bottom-dishes {
    width: 300px;
    height: 150px;
    display: flex;
    padding-right: 150px;
    align-items: flex-start;
    justify-content: flex-end;
    position: relative;
}
.b-d-text {
    color: #ACADB9;
    font-family: 'Poppins';
    font-size: 20px;
    font-weight: 500;
    line-height: 45.18px;
    letter-spacing: -0.10000000149011612px;
    cursor: pointer;
    transition: all 0.3s ease;

}
.b-d-text:hover {
    color: #6C5FBC;
    translate: 0 -5px;
}
.nav-line {
    width: 100%;
    min-width: 300px;
    height: 3px;
    top: -75px;
    background-color: #CBCBCB;
    left: 1px;
    gap: 0px;
    padding-left: 96px;
    padding-right: 96px;
    border: 1px 0px 0px 0px;
    display: flex;
    position: relative;


}
.nav-line-overflow {
    display: flex;
    max-width: 100%;
    min-width: 300px;
    height: 30px;
    
}
.price-dish-h1 {
    font-family: 'Poppins';
    font-size: 25.94px;
    font-weight: 700;
    line-height: 40.34px;
    color: #121826;
}
.price-dish-span {
    font-family: 'Poppins';
    font-size: 18.81px;
    font-weight: 700;
    line-height: 40.34px;
    color: #8E97A6;
    padding-top: 2.5px;

}
.i-f-c-text {
    font-family: 'Poppins';
    font-size: 23.05px;
    font-weight: 600;
    line-height: 37.46px;
}
.price-dish {
    position: absolute;
    left: 15px;
    bottom: 20px;
    display: flex;
    gap: 0;
}
.bottom-i-f-c {
    display: flex;
    width: 300px;
}
.bottom-i-f-c-t {
    font-family: 'Inter';
    font-size: 17.29px;
    font-weight: 400;
    line-height: 23.05px;
    color: #8E97A6;

}
.b-i-f-c-left {
    display: flex;
    gap: 5px;
    width: 300px;
}
.b-i-f-c-right {
    position: absolute;
    right: 15px;
    bottom: 25px;
}
.star-purp {
    width: 20px;
    height: 20px;
}
.food-img {
    width: 201.14px;
    height: 208.19px;
}
.dishes-highlight {
    width: 65.88px;
    height: 24.84px;
    padding-left: 15px;
    padding-right: 15px;
    border-radius: 5.4px;
    background-color: #F7EDD0;
    display: flex;
    align-items: center;
    justify-content: center;


}
.content-food {
    width: 100%;
    height: 100%;
    padding-left: 15px;
}
.highlight-text {
    font-family: 'Poppins';
    font-size: 12.78px;
    font-weight: 400;
    line-height: 19.16px;

}
.heart-image {
    position: absolute;
    right: 20px;
    top: 25px;
}
.foods-cont {
    position: relative;
    display: flex;
    flex-direction: column;
    width: 224.63px;
    height: 390.36px;
    padding-top: 25px;
    border-radius: 34.58px;
    border: 1.44px solid #F4F4F6;
    transition: all 0.5s ease;
}
.foods-cont:hover {
    translate: 0 -15px;
    box-shadow: 6.85px 82.18px 41.09px 0px #E5E5E5B2;
}
.foods-cont5 {
    position: relative;
    display: flex;
    flex-direction: column;
    width: 224.63px;
    height: 390.36px;
    padding-top: 25px;
    border-radius: 34.58px;
    border: 1.44px solid #F4F4F6;
    transition: all 0.5s ease;
}
.foods-cont5:hover {
    translate: 0 -15px;
    box-shadow: 6.85px 82.18px 41.09px 0px #E5E5E5B2;
}
.foods-cont4 {
    position: relative;
    display: flex;
    flex-direction: column;
    width: 224.63px;
    height: 390.36px;
    padding-top: 25px;
    border-radius: 34.58px;
    border: 1.44px solid #F4F4F6;
    transition: all 0.5s ease;
}
.foods-cont4:hover {
    translate: 0 -15px;
    box-shadow: 6.85px 82.18px 41.09px 0px #E5E5E5B2;
}

.root-dishes {
    width: 100%;
    height: 800px;
    display: flex;
    padding-top: 25px;
    flex-direction: column;
    overflow: hidden;
}
.foods {
    width: 100%;
    height: 450px;
    display: flex;
    margin-top: 80px;
    padding-left: 25px;
    padding-right: 25px;
    gap: 15px;
    justify-content: center;
}
.dishes {
    width: 100%;
    height: 493.64px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}
.dishes-text {
    font-family: 'Poppins';
    font-size: 45px;
    font-weight: 600;
    line-height: 25.56px;
    color: #323142;
}
.dishes-span {
    font-family: 'Poppins';
    font-size: 45px;
    font-weight: 600;
    line-height: 25.56px;
    color: #5C4EAE;

}
@media (min-width: 901px) {
    .center-b-d {
            top: -60px;
            height: 100px;
        
    }
    .foods-cont {
        width: 159.74px;
        height: 357.59px;
    }
    .foods-cont5 {
        width: 159.74px;
        height: 357.59px;
        display: flex;
    }
    .foods-cont4 {
        width: 159.74px;
        height: 357.59px;
        display: flex;
    }
    .price-dish {
        left: 15px;
        bottom: 25px;
    }
    .i-f-c-text {
        font-size: 16.39px;
    }
    .food-img {
        width: 143.03px;
        height: 148.05px;
        margin-top: 25px;
    }
    .root-dishes {
        height: 550px;
    }
    .bottom-dishes {
        width: 1000px;
        padding-left: 96px;
        padding-right: 96px;
    }
    .nav-line-overflow {
        padding-left: 96px;
        padding-right: 96px;
    }
}
@media(max-width:900px) {
    .center-b-d {
        top: -60px;
        height: 100px;
    }
    .foods-cont {
        width: 159.74px;
        height: 357.59px;
    }
    .foods-cont5 {
        width: 159.74px;
        height: 357.59px;
        display: none;
    }
    .foods-cont4 {
        width: 159.74px;
        height: 357.59px;
        display: none;
    }
    .price-dish {
        left: 15px;
        bottom: 25px;
    }
    .i-f-c-text {
        font-size: 16.39px;
    }
    .food-img {
        width: 143.03px;
        height: 148.05px;
        margin-top: 25px;
    }
    .foods {
        flex-wrap: wrap;
        margin-top: 40px;
    }
    .root-dishes {
        height: 600px;
    }
    .dishes-text {
        text-align: center;
        width: 200px;
        line-height: 50px;
    }
    .bottom-dishes {
        width: 1000px;
        padding-left: 96px;
        padding-right: 96px;
    }
    .nav-line-overflow {
        padding-left: 96px;
        padding-right: 96px;
    }
    

}
@media (max-width: 600px) {
    .center-b-d {
        top: -60px;
        height: 120px;
    }
    .foods-cont {
        width: 159.74px;
        height: 357.59px;
    }
    .foods-cont5 {
        width: 159.74px;
        height: 357.59px;
        display: none;
    }
    .foods-cont4 {
        width: 159.74px;
        height: 357.59px;
        display: flex;
    }
    .price-dish {
        left: 15px;
        bottom: 25px;
    }
    .i-f-c-text {
        font-size: 16.39px;
    }
    .food-img {
        width: 143.03px;
        height: 148.05px;
        margin-top: 25px;
    }
    .foods {
        flex-wrap: wrap;
        margin-top: 40px;
    }
    .root-dishes {
        height: 550px;
    }
    .dishes-text {
        text-align: center;
        width: 200px;
        line-height: 50px;
    }
    .root-dishes {
        height: 1000px;
    }
    .nav-line-overflow {
        padding-left: 0px;
        padding-right: 0px;
    }
}
@media (min-width: 1186px) {
    .foods {
        flex-wrap: nowrap;
        height: 900px;
    }
    .foods-cont {
        width: 224.63px;
        height: 426.36px;
    }
    .foods-cont5 {
        width: 224.63px;
        height: 426.36px;
        display: flex;
    }
    .foods-cont4 {
        width: 224.63px;
        height: 426.36px;
        display: flex;
    }
    .price-dish {
        left: 15px;
        bottom: 20px;
    }
    .i-f-c-text {
        font-size: 23.05px;
    }
    .food-img {
        width: 201.14px;
        height: 208.19px;
    }
    .root-dishes {
        height: 650px;
    }
    .bottom-dishes {
        width: 1100px;
        padding-right: 0px;
    }
    .nav-line-overflow {
        padding-left: 96px;
        padding-right: 96px;
    }
    .center-b-d {
        top: -60px;
    }


}
</style>