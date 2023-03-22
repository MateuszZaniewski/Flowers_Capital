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
        <div class="indoorplantsWrapper flex6"> 
            <div class="indoorplants__image image">
                <div class="indoorplants--text textstyles">Indoor plants</div>
            </div>
        </div>
        <div class="freshflowersWrapper flex6"> 
            <div class="freshflowers__image image">
                <div class="freshflowers--text textstyles">Fresh flowers</div>
            </div>
        </div>
        <div class="flowerboxesWrapper flex6"> 
            <div class="flowerboxes__image image">
                <div class="flowerboxes--text textstyles">Flower boxes</div>
            </div>
        </div>
        <div class="wreathsWrapper flex6"> 
            <div class="wreaths__image image">
                <div class="wreaths--text textstyles">Wreaths</div>
            </div>
        </div>
        <div class="suculentsWrapper flex6"> 
            <div class="suculents__image image">
                <div class="suculents--text textstyles">Suculents</div>
            </div>
        </div>
        <div class="buqietsWrapper flex6"> 
            <div class="buqiets__image image">
                <div class="buqiets--text textstyles">Bouqets</div>
            </div>
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
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-flow: row wrap;
    width: 90%;
    margin: 0 auto;
    max-width: 1400px;

    .image {
        background-size: cover;
        background-repeat: no-repeat;
        height: 100%;
        width: 100%;
        opacity: 0.8;
    }

    .flex6 {
        display: flex;
        align-items: flex-end;
        justify-content: flex-start;
        position: relative;
    }

    .textstyles {
        color: $gold600;
        font-size: 32px;
        line-height: 38.4px;
        text-align: center;
        background-color: $white100;
        position: absolute;
        width: fit-content;
        width: 100%;
        
    }

    .indoorplantsWrapper {
            

            .indoorplants__image {
                background-image: url('../assets/indoor__plants.png');
                border-radius: 225px 225px 0 0;
                height: 30vw;
                width: 22.569vw;

                .indoorplants--text {
                    top: 60%;
                }

            }
        
    }
    .freshflowersWrapper {


        align-items: flex-start;
            .freshflowers__image {
                background-image: url('../assets/fresh__flowers.png');
                height: 31.25vw;
                width: 22.569vw;

                .freshflowers--text {
                    top: 45%;
                }
            }

         }
    .flowerboxesWrapper {
        position: relative;

        &:before {
            content: '';
            position: absolute;
            z-index: 1;
            transform: translateY(-35%);
            top: 65%;
            left: 10%;
            width: 100%;
            height: 160%;
            border-right: 2px solid $gold600;
        }

        &:after{
            content: '';
            position: absolute;
            z-index: 1;
            transform: translateY(-50%);
            top: 15%;
            left: 0%;
            width: 125%;
            height: 10%;
            border-bottom: 2px solid $gold600;
      
          }

            .flowerboxes__image{
                background-image: url('../assets/flower__boxes.png');
                height: 22.569vw;
                width: 22.569vw;

                .flowerboxes--text {
                    top: 60%
                }
            }
         
         }
    .wreathsWrapper {
        position: relative;

        &:before {
            content: '';
            position: absolute;
            z-index: 1;
            transform: translateY(-35%);
            top: -15%;
            left: -10%;
            width: 100%;
            height: 165%;
            border-left: 2px solid $gold600;
        }

        &:after{
            content: '';
            position: absolute;
            z-index: 1;
            transform: translateY(-50%);
            top: 30%;
            left: -25%;
            width: 125%;
            height: 100%;
            border-bottom: 2px solid $gold600;
      
          }

        align-items: flex-start;
            .wreaths__image{
                background-image: url('../assets/wreaths.png');
                height: 22.569vw;
                width: 22.569vw;

                .wreaths--text {
                    top: 32%;
                }
            }

         }
    .suculentsWrapper {


        align-items: flex-start;
            .suculents__image{
                background-image: url('../assets/suculents.png');
                height: 31.25vw;
                width: 22.569vw;

                .suculents--text {
                    top: 48%;
                }
            }
         
         }
    .buqietsWrapper {


        align-items: flex-start;
            .buqiets__image{
                background-image: url('../assets/buqiets.png');
                border-radius: 0 0 225px 225px;
                height: 30vw;
                width: 22.569vw;

                .buqiets--text {
                    top: 32%;
                }
            }

         }
}


</style>