<template>
    <div class="thedownload">
        <div class="rootdownload">
            <div class="img-mob">
                <img src="/mobile.png" class="img-mobile"/>
            </div>
            <div class="side-text-root">
                <div class="side-text">
                    <h1 class="side-text1">Premium <span class="side-textspan" >Quality</span> For Your Health</h1>
                    <h1 
                    class="side-text2" 
                    v-for="(text,index) in texts"
                    :key="index"
                    :style="{left:text.mg,
                        position:text.pos
                    }"
                    >{{text.text}}</h1>
                    <div class="download-div">
                        <button class="download-button">Download -></button>
                        <img src="/v14.svg" class="image-download" alt="line download">
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
            texts: [
                {
                    text: '⚫︎ Premium quality food is made with ingredients that are packed with essential vitamins, minerals.',
                    mg: '0px',
                    pos:'relative'
                },
                {
                    text: '⚫︎ These foods promote overall wellness by support healthy digestion and boosting immunity',
                    mg: '0px',
                    pos:'relative'
                },
            ]
        }
    }
}
</script>

<style>
.download-button {
    background-color: #6C5FBC;
    width: 186px;
    height: 63px;
    border-radius: 14.68px;
    color: white;
    font-family: 'Inter';
    transition: all 0.5s ease;

}
.image-download {
    position: absolute;
    right: 0;
    top: 50px;

}
.download-button:active {
    scale: 0.9;
}
.download-div {
    width: 334.76px;
    height: 164.97px;
    position: relative;
    display: flex;
    padding: 0px;
    justify-content: space-between;

}
.thedownload {
    width: 100%;
    height: 800px;
    padding-top: 97px;
    padding-left: 127px;
    padding-right: 127px;
    padding-bottom: 97px;
    display: flex;
    justify-content: center;
}
.side-text1 {
    font-family: 'Poppins';
    width: 500px;
    font-size: 50.92px;
    font-weight: 700;
    line-height: 58.2px;
    text-align: left;
    color: black;
    margin-bottom: 25px;
    

}
.side-text2 {
    width: 527.77px;
    height: 61px;
    font-family: 'Inter';
    margin-bottom: 20px;
    font-size: 20px;
    font-weight: 400;
    line-height: 30.5px;
    color: #676767;



}
.side-textspan {
    font-family: 'Poppins';
    font-size: 50.92px;
    font-weight: 700;
    line-height: 58.2px;
    text-align: left;
    color: #5C4EAE;

}
.side-text {
    max-width: 560px;
    min-width: 0px;
    height: 555.97px;
    padding-left: 115px;
    padding-top: 0px;
    padding-bottom: 15px;
    padding-right: 15px;
    display: block;
    position: relative;
    top: 100px;


}
.rootdownload {
    max-width: 1300px;
    min-width: 0px;
    height: 748px;
    display: flex;
    justify-content: space-between;
    gap: 25px;
}
.img-mob {
    height: 625px;
    min-width: 300px;
}
@media (min-width:901px) {
    .rootdownload {
        max-width: 1300px;
        min-width: 0px;
        height: 1000px;
        display: flex;
        padding-bottom: 75px;
        justify-content: space-between;
    }
    .side-text {
        padding-left: 0px;
    }
    .thedownload {
        padding-left: 17px;
        padding-right: 17px;
    }
}
@media (max-width:900px) {
    .thedownload {
        height: 1200px;
    }
    .rootdownload {
        max-width: 1300px;
        min-width: 0px;
        height: 1200px;
        display: flex;
        padding-bottom: 75px;
        flex-direction: column-reverse;
        justify-content: center;
    }
    .side-text {
        padding-left: 0px;
    }
    .thedownload {
        padding-left: 17px;
        padding-right: 17px;
        
    }
}
@media (max-width:600px) {
    .rootdownload {
        max-width: 1300px;
        min-width: 0px;
        height: 700px;
        display: flex;
        padding-top: 75px;
        flex-direction: column-reverse;
        justify-content: center;
    }
    .thedownload {
        height: 700px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-end;
    }
    .img-mobile {
        max-height: 300px;
        position: relative;
        top: 0px;

    }
    .img-mob {
        width: 100%;
        height: 300px;
        padding-left: 30px;
        position: relative;
        display: flex;
        justify-content: center;
    }
    .side-text-root {
        display: flex;
        flex-direction: row;
        justify-content: center;
        height: 400px;
        align-items: flex-end;
        position: relative;
        top: 170px;
    }
    .download-div {
        align-items: center;
        flex-direction: column;
    }
    .side-text {
        padding: 0px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;

    }
    .download-button {
        width: 121.77px;
        height: 41.24px;
        border-radius: 9.61px;

    }
    .image-download {
        rotate: 110deg;
        left: 0;
        scale: 0.5;
    }
    .side-text1 {
        font-size: 30px;
        font-weight: 700;
        width: 300px;
        line-height: 34.23px;
        text-align: center;

    }
    .side-text2 {
        font-size: 11.96px;
        line-height: 17.94px;
        text-align: left;
        width: 315px;
        margin-bottom: 0px;
        height: 50px;

    }
    .side-textspan {
        font-size: 30px;
    }
}


</style>