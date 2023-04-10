<script setup>
const windowWidth = window.innerWidth;
</script>

<template>
    <div class="desktopQuery">
        <div class="FlexImagesWrapper">
            <div class="image__container1">
                <div class="image1 image"></div>
                <div class="image4 image"></div>
            </div>
            
            <div class="image__container2">
                <div class="image2 image"></div>
                <div class="image5 image"></div>
            </div>
           
            <div class="image__container3">
                <div class="image3 image"></div>
                <div class="image6 image"></div>
            </div>
            
        </div>
    
        <div class="checkWrapper">
            <h2>Check how we do it</h2>
            <button>Go to gallery</button>
        </div>
    </div>
    
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.FlexImagesWrapper {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    padding-bottom: 36px;
    
    
    .image__container1, .image__container2 {
        display: flex;
        flex-flow: column nowrap;
        padding-right: 8px;
        gap: 8px;
    }

    .image__container3 {
        display: flex;
        flex-flow: column nowrap;
        gap: 8px;
    }

    .image {
        width: 29.231vw;
        height: 29.231vw;
        background-repeat: no-repeat;
        background-size: cover;
    }

    .image1 {
        height: 43.59vw;
        background-image: url('../assets/howwedo1.png');
        border-radius: 180px 180px 0 0;
    }

    .image2 {
        background-image: url('../assets/howwedo2.png');
    }

    .image3 {
        height: 43.59vw;
        background-image: url('../assets/howwedo3.png');
        border-radius: 180px 180px 0 0;
    }

    .image4 {
        background-image: url('../assets/howwedo4.png');
    }

    .image5 {
        height: 43.59vw;
        background-image: url('../assets/howwedo5.png');
    }

    .image6 {
        background-image: url('../assets/howwedo6.png');
    }
}

.checkWrapper {

    width: 56.923vw;
    margin: 0 auto;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    padding-bottom: 56px;


    h2 {
        font-size: $mobileH1;
        color: $gold600;
        line-height: 52.8px;
        text-align: center;

    }

    button {
        padding: 15px 40px 15px 40px;
        background: $gold600;
        font-size: $mobileBody;
        border-radius: 40px;
        color: $white100;
        border: none;
        line-height: 27.6px;
        margin-top: 13px;
    }

    button:hover {
        background: $gold700;
      }
}


@media screen and (min-width: 1024px) {

    .desktopQuery {
        display: flex;
        flex-flow: row;
        flex-direction: row-reverse;
        padding-bottom: 140px;
        max-width: 1440px;
        margin: 0 auto;

        .FlexImagesWrapper {
            display: flex;
            flex-flow: row wrap;
            justify-content: center;
            padding-bottom: 36px;
            width: 70%;
            
            
            .image__container1, .image__container2 {
                display: flex;
                flex-flow: column nowrap;
                padding-right: 20px;
                gap: 20px;
                padding-top: 50px;
            }

            .image__container2 {
                padding-top: 0;
            }
        
            .image__container3 {
                display: flex;
                flex-flow: column nowrap;
                gap: 20px;
                padding-top: 50px;
            }
        
            .image {
                width: 17.361vw;
                height: 17.361vw;
                background-repeat: no-repeat;
                background-size: cover;
            }
        
            .image1 {
                height: 26.042vw;
                background-image: url('../assets/howwedo1.png');
                border-radius: 180px 180px 0 0;
            }
        
            .image2 {
                background-image: url('../assets/howwedo2.png');
            }
        
            .image3 {
                height: 26.042vw;
                background-image: url('../assets/howwedo3.png');
                border-radius: 180px 180px 0 0;
            }
        
            .image4 {
                background-image: url('../assets/howwedo4.png');
            }
        
            .image5 {
                height: 26.042vw;
                background-image: url('../assets/howwedo5.png');
            }
        
            .image6 {
                background-image: url('../assets/howwedo6.png');
            }
        }
        
        .checkWrapper {
        
            margin-left: 40px;
            display: flex;
            flex-flow: column nowrap;
            align-items: center;
            justify-content: center;
            padding-bottom: 0;
            width: 30%;
        
        
            h2 {
                font-size: $desktopH1;
                color: $gold600;
                line-height: 85.14px;
                text-align: center;
        
            }
        
            button {
                padding: 15px 40px 15px 40px;
                background: $gold600;
                font-size: 28px;
                border-radius: 40px;
                color: $white100;
                border: none;
                line-height: 33.6px;
                margin-top: 60px;
            }

            button:hover {
                background: $gold700;
              }
        }
    }

}

</style>