<script setup>
const windowWidth = window.innerWidth;
</script>

<template>
    <div id="shop" class="shopWrapper">
        <h2>Shop</h2> 
        <div class="shopInfos">
            <h3>We offer convenient online ordering and delivery services.</h3>
            <p>You can choose from indoor plants, forever green suculents, colorful wreaths and flower crowns, stunning flower boxes, already made bouquets or fresh flowers to make your own composition.</p>
            <p>Discover our offer, select your desired flowers or plants, and we'll take care of the rest.</p>
            <button>Go to our shop</button>
        </div>
        <img class="greyFlower2" src="../assets/greyFlower2.png" />
    </div>
    <div class="shop__categories">
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
    display: flex;
    max-width: 2000px;
    margin: 0 auto;

        h2 {
        transform: rotate(180deg);
        white-space: nowrap;
        color: $gold600;
        margin: 0;
        width: fit-content;
        position: absolute;
        z-index: 100;
        top: 0%;
        left: 4%;
        writing-mode: vertical-lr;
        font-size: 35px;
        
      }

    .shopInfos {
        width: 80%;
        margin-right: 32px;
        margin-left: clamp(10px, 20vw, 180px);
        padding-bottom: $spc36;
        z-index: 100;

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
            font-size: $mobileBody;
            border-radius: 40px;
            border: none;
            color: $white100;
        }

        button:hover {
            background: $gold700;
          }
    }
    
    .greyFlower2 {
        position: absolute;
        top: 5%;
        right: 0;
    }
}

.shop__categories {
    display: none;
}


@media screen and (min-width: 1024px) {
    .shopWrapper {

        h2 {
            font-size: 44px;
        }

        .shopInfos {
            width: 80%;
            margin-right: 32px;
            margin-left: clamp(10px, 20vw, 180px);
            padding-bottom: $spc36;
            z-index: 100;
    
            h3 {
                font-size: 2.222vw;
                line-height: 2.361vw;
                color: $black900;
                margin: 0;
                padding-bottom: 40px;
    
            }
    
            p {
                font-size: 1.597vw;
                line-height: 1.917vw;
                color: $black900;
                margin: 0;
                padding-bottom: 20px;
            }
    
            button {
                display: none;
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
        max-width: 2000px;
        padding-top: 120px;
        padding-bottom: 160px;
    
        .image {
            background-size: cover;
            background-repeat: no-repeat;
            height: 100%;
            width: 100%;
            opacity: 1;
    
            &:hover{
                opacity: 0.8;
            }
        }
    
        .flex6 {
            display: flex;
            align-items: flex-end;
            justify-content: flex-start;
            position: relative;
            cursor: pointer;
        }
    
        .textstyles {
            color: $gold600;
            font-size: 2.222vw;
            line-height: 2.667vw;
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
                left: 105%;
                width: 5%;
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
                width: 5%;
                height: 165%;
                border-left: 2px solid $gold600;
            }
    
            &:after{
                content: '';
                position: absolute;
                z-index: 1;
                transform: translateY(-50%);
                top: 77%;
                left: -25%;
                width: 125%;
                height: 5%;
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
}

</style>