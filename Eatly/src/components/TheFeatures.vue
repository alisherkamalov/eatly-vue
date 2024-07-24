<template>
    <section class="w-full h-56 bg-purple relative">
        <div class="w-full h-56 flex justify-start absolute">
            <img src="/v1.svg" class="v1">
            <img src="/v2.svg" class="v2">
        </div>
        <div class="absolute flex justify-center content-center w-full h-56">
            <ul class="flex w-full h-56 justify-center">
                <li class="block text-center content-center w-64 h-56">
                    <h1 class="textl1">
                        10K+
                    </h1>
                    <div class="w-64 h-auto flex px-25 text-center content-center">
                        <h1 class="textl2-1">
                            Satisfied Costumers All Great Over The World
                        </h1>
                    </div>
                    
                </li>
                <div class="w-px h-56 block justify-center content-center">
                    <div class="w-px h-32 bg-grey">
                    </div>
                </div>
                
                <li class="block text-center content-center w-64 h-56">
                    <h1 class="textl1">
                        4M
                    </h1>
                    <div class="w-64 h-auto flex px-25 text-center content-center">
                        <h1 class="textl2-2">
                            Healthy Dishes Sold Including Milk Shakes Smooth
                        </h1>
                    </div>
                </li>
                <div class="w-px h-56 block justify-center content-center">
                    <div class="w-px h-32 bg-grey">
                    </div>
                </div>
                <li class="block text-center content-center w-64 h-56">
                    <h1 class="textl1">
                        99.99%
                    </h1>
                    <div class="w-64 h-auto flex px-25 text-center content-center">
                        <h1 class="textl2-3">
                            Reliable Customer Support We Provide Great Experiences
                        </h1>
                    </div>
                </li>
            </ul>
        </div>
        <div class="w-full h-56 flex justify-end absolute">
            <img src="/v3.svg" class="v3">
            <img src="/v4.svg" class="v4">
        </div>
        
        

    </section>
</template>
<script>
</script>
<style>
.text-center {
    justify-content: center;
}
.textl1 {
    color: white;
    font-family: 'Inter';
    font-size: 43px;
    font-weight: 700;
}
.textl2-1 {
    color: #C5BFED;
    font-family: 'Inter';
    font-size: 14.4px;
    font-weight: 500;
    width: 165px;
    line-height: 21.6px;
    text-align: center;

}
.textl2-2 {
    color: #C5BFED;
    font-family: 'Inter';
    font-size: 14.4px;
    font-weight: 500;
    width: 206px;
    line-height: 21.6px;
    text-align: center;

}
.textl2-3 {
    color: #C5BFED;
    font-family: 'Inter';
    font-size: 14.4px;
    font-weight: 500;
    width: 208px;
    line-height: 21.6px;
    text-align: center;

}
.v1 {
    position: absolute;
    justify-content: start;
    left: 0px;
    top: 0px;
}
.v2 {
    position: absolute;
    justify-content: start;
    left: 0px;
    top: 0px;
}
.v3 {
    position: absolute;
    justify-content: end;
    right: 0px;
    top: 0px;
}
.v4 {
    position: absolute;
    justify-content: end;
    right: 0px;
    top: 0px;
}
@media (max-width:799px) { 
    section.w-full.h-56.bg-purple.relative {
        height: 748px;
        margin-top: 75px;
        display: flex;
        flex-direction: column;

    }
    div.absolute.flex.justify-center.content-center.w-full.h-56 {
        display: block;
    }
    ul.flex.w-full.h-56.justify-center {
        display: flex;
        flex-direction: column;
        height: 748px;
        justify-content: center;
        align-items: center;
    }
    div.w-px.h-56.block.justify-center.content-center {
        height: 1px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    div.w-px.h-32.bg-grey {
        width: 246px;
        height: 1px;
    }
    div.w-full.h-56.flex.justify-start.absolute {
        display: none;
    }
    div.w-full.h-56.flex.justify-end.absolute {
        display: none;
    }


}
</style>