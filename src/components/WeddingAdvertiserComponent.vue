<script setup>

</script>

<template>
    <div id="weddings" class="mobileAndTabletView">
        <div class="weddingWrapper">
            <div class="weddingFoto"></div>
            <div class="weddingText">
                <h3>We make your special day unforgettable</h3>
            </div>
        </div>
    </div>
    <div id="weddings" class="desktopView">
        <div class="weddingWrapper">
            <div class="weddingFoto">
                <div class="weddingText">
                    <h3>We make your special day unforgettable</h3>
                </div>
                
            </div>
        </div>
    </div>
    
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

.desktopView {
    display: none;
}

.mobileAndTabletView {
    padding-bottom: 40px;
    
    .weddingFoto {
        height: 67.949vw;
        width: 100%;
        background-image: url('../assets/weddingfullwidth.png');
        background-repeat: no-repeat;
        background-size: cover;
    }
    
    .weddingText {
    
        text-align: center;
        padding-top: 16px;
        max-width: 760px;
        margin: 0 auto;
    
        h3 {
            font-size: $mobileH1;
            color: $gold600;
            line-height: 52.8px;
            margin: 0;
            padding: 0;
    
        }
    }

}

@media screen and (min-width: 1024px) {

    .mobileAndTabletView {
        display: none;
    }

    .desktopView {
        display: block;
        padding-bottom: 100px;
        max-width: 1500px;
        margin: 0 auto;
    
        .weddingFoto {
            height: 43.571vw;
            width: 100%;
            position: relative;
    
            &:before{
                content: "";
                background-image: url('../assets/weddingfullwidthDesktop.png');
                background-size: cover;
                position: absolute;
                top: 0px;
                right: 0px;
                bottom: 0px;
                left: 0px;
            }
    
            .weddingText {
                
                h3 {
                    font-size: $desktopH1;
                    color: $gold600;
                    line-height: 85.14px;
                    margin: 0;
                    position: absolute;
                    bottom: 30px;
                    z-index: 100;
                    text-align: center;
                    
            
                }
    
            }
    
            
    
        }
    }
}





//43.571vw

</style>