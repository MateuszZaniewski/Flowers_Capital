<script setup>
const windowWidth = window.innerWidth;
</script>

<template>
    <div class="shopWrapper">
        <h2>Shop</h2> 
        <div class="shopInfos">
            <h3>We offer convenient online ordering and delivery services.</h3>
            <p>You can choose from indoor plants, forever green suculents, colorful wreaths and flower crowns, stunning flower boxes, already made bouquets or fresh flowers to make your own composition.</p>
            <p>Discover our offer, select your desired flowers or plants, and we'll take care of the rest.</p>
            <button v-if="windowWidth < 1024">Go to our shop</button>
        </div>
    </div>
    <div class="shop__categories" v-if="windowWidth >= 1024">
        <div class="indoorplantsWrapper"> 
            <div class="indoorplants__image image"></div>
        </div>
        <div class="freshflowersWrapper"> 
            <div class="freshflowers__image image"></div>
        </div>
        <div class="flowerboxesWrapper"> 
            <div class="flowerboxes__image image"></div>
        </div>
        <div class="wreathsWrapper"> 
            <div class="wreaths__image image"></div>
        </div>
        <div class="suculentsWrapper"> 
            <div class="suculents__image image"></div>
        </div>
        <div class="buqietsWrapper"> 
            <div class="buqiets__image image"></div>
        </div>
    </div>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.shopWrapper {
    position: relative;
    padding-top: $spc72;
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
        top: 10%;
        left: 4%;
        writing-mode: vertical-lr;
        font-size: $mobileH2;
        
      }

    .shopInfos {
        width: 80%;
        margin-right: 32px;
        margin-left: clamp(10px, 20vw, 130px);

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

.shop__categories {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 40px;
    grid-row-gap: 40px;
    width: 90%;
    margin: 0 auto;

    .image {
        background-size: cover;
        background-repeat: no-repeat;
        height: 100%;
        width: 100%;
    }

    .indoorplantsWrapper { 
        grid-area: 1 / 1 / 2 / 2; 
        height: 100%;
        width: 100%;
        border: 1px solid green;

            .indoorplants__image {
                background-image: url('../assets/indoor__plants.png');
                border-radius: 225px 225px 0 0;
            }
        
    }
    .freshflowersWrapper {
         grid-area: 1 / 2 / 2 / 3;
         height: 100%;
         width: 100%;
         border: 1px solid green;
            .freshflowers__image {
                background-image: url('../assets/fresh__flowers.png');
            }

         }
    .flowerboxesWrapper {
         grid-area: 1 / 3 / 2 / 4;
         height: 31.25vw;
         width: 100%;
         border: 1px solid green;
            .flowerboxes__image{
                background-image: url('../assets/flower__boxes.png');
            }
         
         }
    .wreathsWrapper {
         grid-area: 2 / 1 / 3 / 2;
         height: 31.25vw;
         width: 100%;
         border: 1px solid green;
            .wreaths__image{
                background-image: url('../assets/wreaths.png');
            }

         }
    .suculentsWrapper {
         grid-area: 2 / 2 / 3 / 3;
         height: 31.25vw;
         width: 100%;
         border: 1px solid green;
            .suculents__image{
                background-image: url('../assets/suculents.png');
            }
         
         }
    .buqietsWrapper {
         grid-area: 2 / 3 / 3 / 4;
         height: 100%;
         width: 100%;
         border: 1px solid green;
            .buqiets__image{
                background-image: url('../assets/buqiets.png');
                border-radius: 0 0 225px 225px;
            }

         }
}


</style>