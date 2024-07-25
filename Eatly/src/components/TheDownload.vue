<template>
    <div class="thedownload">
        <div class="rootdownload">
            <div class="w-96">
                <img src="/mobile.png"/>
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
                    mg: '-7px',
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
.w-96 {
    height: 625px;
}

@media (min-width:300px) {
    .download-button {
        border-radius: 9.61px;
        width: 121.77px;
        height: 41.24px;


    }
    .image-download {
        left: 0px;
        bottom: 0;
        rotate: 110deg;
        scale: 0.5;
        top: 30px;
    }
    .side-text2 {
        font-size: 11.96px;
        width: 315px;
        text-align: center;
    }
    .download-div {
        padding: 0;
        margin: 0;
        justify-content: center;
    }
    .side-text1 {
        width: 300px;
        font-size: 30px;
        justify-content: center;
        line-height: 34.23px;
        text-align: center;

    }
    .side-textspan {
        font-size: 30px;
    }
    .thedownload {
        padding-top: 250px;
        height: auto;
    }
    .side-text-root {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .side-text {
        display: flex;
        flex-direction: column;
        padding-left: 0px;
        margin-top: 60px;
        height: auto;
        align-items: center;
    }
    .rootdownload {
        display: flex;
        flex-wrap: nowrap;
        flex-direction: column-reverse;
        height: 550px;
        align-items: center;
    }
    .w-96 {
        width: 200px;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-left: -10px;
    }
}

@media (min-width:600px) {
    .thedownload {
        padding-top: 50px;
        height: 1000px;
    }
    .side-text-root {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .side-text {
        padding-left: 0px;
        padding-top: 50px;
    }
    .rootdownload {
        display: flex;
        flex-wrap: nowrap;
        flex-direction: column-reverse;
        height: 1000px;
    }
    .w-96 {
        width: 100%;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-left: 25px;
        scale: 0.8;
        top: -50px;
        left: 10px;
    }
}
@media(min-width:900px) {
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
        right: 0px;
        top: 0px;
        left: auto;
        bottom: 0;
        rotate: 0deg;
        scale: 1;
        top: auto;
        bottom: 50px;
        
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
        overflow: hidden;
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
        padding: 0;
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
        top: -10px;
    
    
    }
    .rootdownload {
        max-width: 1300px;
        min-width: 0px;
        height: 748px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 25px;
        
    }
    .w-96 {
        scale: 5;
        height: 625px;
    }
    .side-text-root {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: start;
    }
}
@media (min-width:1000px) {
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
        right: 0px;
        top: 0px;
        left: auto;
        bottom: 0;
        rotate: 0deg;
        scale: 1;
        top: auto;
        bottom: 50px;
        
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
        padding: 0;
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
        top: -10px;
    
    
    }
    .rootdownload {
        max-width: 1300px;
        min-width: 0px;
        height: 748px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 25px;
    }
    .w-96 {
        scale: 1.5;
        height: 625px;
        top: -100px;
    }
    .side-text-root {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: start;
    }
}
@media (min-width:1086px) {
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
        right: 0px;
        top: 0px;
        left: auto;
        bottom: 0;
        rotate: 0deg;
        scale: 1;
        top: auto;
        bottom: 50px;
        
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
        padding: 0;
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
        top: -10px;
    
    
    }
    .rootdownload {
        max-width: 1300px;
        min-width: 0px;
        height: 748px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 25px;
    }
    .w-96 {
        scale: 1;
        height: 625px;
    }
    .side-text-root {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: start;
    }

    
}

</style>