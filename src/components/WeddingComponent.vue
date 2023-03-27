<script setup>
console.log('hello script setup')
</script>

<template>
    <div class="weddingComponentWrapper">
        <h2>Weddings</h2> 
        <div class="weddingInfos">
            <p>Flowers'Capital offers beautiful and personalized wedding floral arrangements. Our experienced team of florists will work with you to bring your vision to life, whether you want a classic, romantic, or modern theme. Our goal is to bring your dream wedding to life with stunning floral arrangements that will leave a lasting impression on you and your guests.</p>
        </div>
    </div>
    <div class="weddingComponentFotoWrapper">
        <div class="fotoWrapper wrap1">
            <div class="foto1"></div>
        </div>
        <div class="fotoWrapper wrap2">
            <div class="foto2"></div>
        </div>
        <div class="fotoWrapper wrap3">
            <div class="foto3"></div>
        </div>
        <div class="fotoWrapper wrap4">
            <div class="foto4"></div>
        </div>
    </div>
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

.weddingComponentWrapper {
    position: relative;
    display: flex;
    max-width: 1400px;
    margin: 0 auto;

    h2 {
        transform: rotate(180deg);
        white-space: nowrap;
        color: $gold600;
        margin: 0;
        width: fit-content;
        position: absolute;
        z-index: 1;
        top: 0%;
        left: 4%;
        writing-mode: vertical-lr;
        font-size: $mobileH2;
        
      }


    .weddingInfos {
        width: 80%;
        margin-right: 32px;
        margin-left: clamp(10px, 20vw, 130px);
        padding-bottom: $spc36;

        h3 {
            font-size: $mobileH3;
            line-height: 34px;
            color: $black900;
            margin: 0;
            padding-bottom: 40px;

        }

        p {
            font-size: $mobileBody;
            line-height: 27px;
            color: $black900;
            margin: 0;
            padding-bottom: 20px;
        }

        button {
            padding: 15px 40px 15px 40px;
            background: $gold600;
            font-size: $mobileH4;
            border-radius: 40px;
            color: $white100;
            border: none;
            line-height: 27.6px;
            margin-top: 13px;
        }
    }
    
}

.weddingComponentFotoWrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-right: 16px;
    margin-left: 16px;


    .fotoWrapper {
        display: flex;

        .foto1 {
            background-image: url('../assets/foto1.png');
            background-size: cover;
            background-repeat: no-repeat;
            width: 43.333vw;
            height: 55.385vw;
        }

        .foto2 {
            background-image: url('../assets/foto2.png');
            background-size: cover;
            background-repeat: no-repeat;
            width: 31.538vw;
            height: 37.436vw;
            align-self: flex-end;
            position: relative;

            &:before {
                content: '';
                position: absolute;
                z-index: 1;
                transform: translateY(-35%);
                top: -10%;
                left: 0%;
                width: 125%;
                height: 5%;
                border-top: 2px solid $gold600;
            }
    
        }

        .foto3 {
            background-image: url('../assets/foto3.png');
            background-size: cover;
            background-repeat: no-repeat;
            width: 31.538vw;
            height: 37.436vw;
            position: relative;

            &:before {
                content: '';
                position: absolute;
                z-index: 1;
                transform: translateY(-35%);
                top: 45%;
                left: -15%;
                width: 100%;
                height: 125%;
                border-left: 2px solid $gold600;
            }
    
            &:after{
                content: '';
                position: absolute;
                z-index: 1;
                transform: translateY(-50%);
                top: 110%;
                left: -25%;
                width: 125%;
                height: 5%;
                border-bottom: 2px solid $gold600;
          
              }
        }

        .foto4 {
            background-image: url('../assets/foto4.png');
            background-size: cover;
            background-repeat: no-repeat;
            width: 43.333vw;
            height: 55.385vw;
        }
    }

}


</style>