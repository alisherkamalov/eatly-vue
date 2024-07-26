<template>
    <div class="rest-root">
        <div class="rest-content">
            <h1 class="text-rest">
                Our Top <span class="span-rest">Restaurants</span>
            </h1>
            <div class="resturent-root">
                <div class="resturent-cont" v-for="(rest,index) in rests" :key="index">
                    <div class="rest-image">
                        <img :src="rest.image"/>
                    </div>
                    <div class="rest-info">
                        <div class="rest-highlight"
                        :style="{
                            backgroundColor: rest.highcolor
                        }">
                            <h1 class='highlight-text' 
                            :style="{
                                color: rest.highcolortext
                            }">{{rest.hightext}}</h1>
                        </div>
                        <div class="info-rest-content">
                            <h1 class="i-r-c-text">{{rest.text}}</h1>
                        </div>
                        <div class="bottom-i-r-c">
                            <div class="b-i-r-c-left">
                                <h1 class="bottom-i-r-c-t">{{rest.minutes}}</h1>
                                <img src="/star-purple.png" class="star-purp"/>
                                <h1 class="bottom-i-r-c-t">{{rest.rating}}</h1>
                            </div>
                            <div class="b-i-r-c-right"> 
                                <img src="/bookmark.png"/>
                            </div>
                            
                        </div>
                    </div>
                </div>  
            </div>
        </div>
    </div>
</template>
<script>

export default {
    data() {
        return {
            rests: [
                {
                    text:'The Chicken King',
                    image: '/rest1.png',
                    hightext:'Healthy',
                    highcolor:'#F7EDD0',
                    highcolortext:'#DAA31A',
                    minutes:'24min •',
                    rating:'4.8'
                },
                {
                    text:'The Burger King',
                    image: '/rest2.png',
                    hightext:'Trending',
                    highcolor:'#F7C5BA',
                    highcolortext:'#FB471D',
                    minutes:'24min •',
                    rating:'4.9'
                },
                {
                    text:'The Chicken King',
                    image: '/rest1.png',
                    hightext:'Healthy',
                    highcolor:'#F7EDD0',
                    highcolortext:'#DAA31A',
                    minutes:'24min •',
                    rating:'4.8'
                },

            ]
        }
    }
}
</script>
<style>
.bottom-i-r-c {
    display: flex;
    gap: 5px;
    width: 100%;
    justify-content: space-between;
}
.b-i-r-c-left {
    display: flex;
    gap: 5px;
}
.b-i-r-c-right {
    position: absolute;
    right: 25px;
    bottom: 15px;
}
.star-purp {
    width: 25.79px;
    height: 25.79px;

}
.rest-info {
    display: flex;
    flex-direction: column;
    padding-left: 25px;
    padding-right: 25px;
    padding-top: 15px;
}
.bottom-i-r-c-t {
    font-family: 'Inter';
    font-size: 19.34px;
    font-weight: 400;
    line-height: 25.79px;
    color: #8E97A6;

}
.i-r-c-text {
    font-family: 'Poppins';
    font-size: 25.79px;
    font-weight: 600;
    line-height: 41.9px;
    color: black;

}
.highlight-text {
    font-family: 'Poppins';
    font-size: 12.78px;
    font-weight: 400;
    line-height: 19.16px;

}
.resturent-cont {
    width: 395.99px;
    height: 297.6px;
    border-radius: 30.02px;
    display: flex;
    flex-direction: column;
    border: 1.25px solid #F4F4F6;
    position: relative;
    overflow: hidden;
    transition: all 0.5s ease;
}
.resturent-cont:hover {
    box-shadow: 5.95px 71.35px 35.67px 0px #E5E5E5B2;
    translate: 0px -10px;
}
.rest-highlight {
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

.resturent-root {
    width: 1248.95px;
    height: 297.6px;
    display: flex;
    padding-left: 35px;
    padding-right: 35px;
    gap: 15px;
}
.text-rest {
    font-family: 'Poppins';
    font-size: 45px;
    font-weight: 600;
    line-height: 25.56px;
    text-align: center;
    color: black;
}
.span-rest {
    font-family: Poppins;
    font-size: 45px;
    font-weight: 600;
    line-height: 25.56px;
    text-align: center;
    color: #5C4EAE;

}
.rest-root {
    width: 100%;
    height: 641px;
    display: flex;
    padding-left: 96px;
    padding-right: 96px;
    justify-content: center;
    overflow: hidden;
    padding-top: 150px;
}
.rest-content {
    max-width: 1248.95px;
    min-width: 300px;
    display: flex;
    gap: 100px;
    flex-direction: column;
    align-items: center;
}
@media (min-width:701px) {
    .resturent-cont {
        width: 401.6px;
    }
    .resturent-root {
        width: 750.6px;
    }
    .b-i-r-c-right {
        right: 10px;
        bottom: 10px;
    }
}
@media (max-width:700px) {
    
    .resturent-cont {
        width: 315px;
    }
    .text-rest {
        height: 50px;
        line-height: 50px;
    }
    .resturent-root {
        flex-direction: column;
        height: auto;
        justify-content: center;
        width: 315px;
        padding-left: 0px;
        padding-right: 0px;
    }    
    .rest-content {
        min-width: 315px;
        padding-left: 0px;
        padding-right: 0px;
    }
    .rest-root {
        height: 1200px;
        justify-content: center;
        padding-top: 50px;
    }
}

@media (min-width:1101px) {
    .resturent-cont {
        width: 1001.6px;
    }
    .resturent-root {
        width: 1050.6px;
    }
}
</style>