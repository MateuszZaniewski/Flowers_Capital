<script setup>
const piwoniaDesktop = '../src/assets/piwoniaDesktop.png'
const piwoniaMobile = '../src/assets/piwoniaMobile.png'
function piwoniaImageResizer() {
    return window.innerWidth < 1100 ? piwoniaMobile : piwoniaDesktop
}
console.log(piwoniaImageResizer)
</script>

<template>
    <main>
        <div class="heroImageWrapper">
            <div>
                <img :src="piwoniaImageResizer()" />
            </div>
            
        </div>
        <div class="mainTextWrapper">
            <h1>
                Welcome to our world of flowers
            </h1>
        </div>
        
        <div class="downWrapper">
            <img src="../assets/downPage.png" />
        </div>
    </main>
    <div>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
        <p>x</p>
    </div>
    
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

main {
    background: $white100;

    h1 {
        font-size: $mobileH1;
        line-height: 52.8px;
        letter-spacing: -2%;
        text-align: center;
        color: $gold600;
        padding-top: $spc32;
    }
}

.mainTextWrapper{
    text-align: center;
}

.heroImageWrapper {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    background: $white100;

    img {
        max-height: 100%;
        max-width: 100%;
        object-fit: cover;
        max-height: 900px;
        margin: 0;
    }
}

.downWrapper{
    display: flex;
    justify-content: center;
    padding-top: $spc72;
}

@media screen and (min-width: 1100px) {

    main {
        background: $white100;
        display: flex;
        flex-direction: row-reverse;
        align-items: center;
        width: 100%;
        margin: 0 auto;
        max-width: 2000px;
    
        h1 {
            font-size: $desktopH1;
            line-height: 85.14px;
            text-align: center;
            color: $gold600;
            
            margin: 0;
            padding: 0;
        }

        .heroImageWrapper{
            width: 60%;
        }
        
        .mainTextWrapper{
            width: 40%;
            text-align: center;
            margin: 0 auto;
        }

        .downWrapper{
            display: none;
        }
    }

    .heroImageWrapper {
        display: flex;
        justify-content: flex-end;
        align-items: center;
    
        img {
            max-height: 100%;
            max-width: 100%;
            object-fit: cover;
            max-height: 900px;
            margin: 0;
        }
    }
}

@media screen and (min-width: 600px) and (min-width: 1099px) {
    .heroImageWrapper {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        width: 90%;
        float: right;
    
        img {
            max-height: 100%;
            max-width: 100%;
            object-fit: cover;
            max-height: 900px;
            margin: 0;
        }
    }
}

</style>

