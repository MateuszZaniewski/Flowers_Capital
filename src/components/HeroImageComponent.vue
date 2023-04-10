<script setup>

const scrollDown = () => {
  let scrollPosition = 0
  const heightOfScreen = window.innerHeight
  scrollPosition += heightOfScreen
  window.scrollTo({ top: scrollPosition, behavior: 'smooth' });
};
</script>

<template>
    <main>
        <div class="heroImageComponentWrapper">
            <div class="heroImageWrapper">
                <div class="heroImage__image"></div>
            </div>
            <div class="heroImageText">
                <h1>Welcome to our world of flowers</h1>
            </div>
        </div>
        <div class="downWrapper">
            <img src="../assets/downPage.png"  @click="scrollDown()"/>
        </div>
    </main>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.heroImageComponentWrapper {
    display: flex;
    flex-flow: column nowrap;

    h1 {
        text-align: center;
        color: $gold600;
        font-size: $mobileH1;
        padding-top: 20px;
        line-height: 52.8px;
    }

    .heroImageWrapper {
        display: flex;
        height: auto;
        width: auto;
        justify-content: flex-end;
        

        .heroImage__image {
            background-image: url('../assets/mobileSlice.png');
            background-repeat: no-repeat;
            background-size: cover;
            height: 126.41vw;
            width: 100%;
            max-width: 500px;
            max-height: 700px;
        }

    }
}   

.downWrapper {
        display: flex;
        justify-content: center;
        padding-top: 11.282vh;
        padding-bottom: 24.615vw;
}

@media screen and (min-width: 500px) and (max-width: 1023px) {
    .downWrapper {
        display: none;
    }

    .heroImageComponentWrapper {
        padding-bottom: 150px;
    }
}


@media screen and (min-width: 1024px) {

    main {
        padding-bottom: 100px;
        max-width: 1600px;
        margin: 0 auto;
    }

    .heroImageComponentWrapper {
        display: flex;
        flex-flow: row nowrap;
        flex-direction: row-reverse;
    
        h1 {
            text-align: center;
            color: $gold600;
            font-size: $desktopH1;
            padding-top: 20px;
            text-align: left;
            line-height: 85.14px;
        }

        .heroImageText {
            display: flex;
            flex-flow: column;
            justify-content: center;
            width: 45%;
            padding-left: 40px;
            
        }
    
        .heroImageWrapper {
            display: flex;
            height: auto;
            width: 60%;
            justify-content: flex-end;
            
    
            .heroImage__image {
                background-image: url('../assets/slice4.png');
                background-repeat: no-repeat;
                background-size: cover;
                height: 126.41vw;
                width: 100%;
                max-width: auto;
                max-height: auto;
            }
    
        }
    }   
    
    .downWrapper {
            display: none;
    }
}

</style>

