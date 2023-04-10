<script setup>
import { ref } from 'vue';

let toggled = ref(true)

function isToggled() {
    toggled.value = !toggled.value
    console.log(toggled.value)
}   
</script>

<template>
        <header :style="{ background: !toggled ? '#F9F8F9' : 'transparent'}">
            <div class="mobileHeader">
                <div v-if="toggled" class="hamburger" @click="isToggled">
                    <span class="hamburger--bar bartop"></span>
                    <span class="hamburger--bar barmiddle"></span>
                    <span class="hamburger--bar barbottom"></span>
                </div>
                <div v-if="!toggled" class="hamburger__closed" @click="isToggled">
                    <span class="hamburger--x x-one"></span>
                    <span class="hamburger--x x-two"></span>
                </div>
                    <p class="logoText">Flower's Capital</p>
            </div>
            <div class="desktopHeader">
                <div class="desktopWrapper">
                    <div class="desktop__spansWrapperLeft flexCenter">
                        <span class="redirect--span">ABOUT US</span>
                        <span class="redirect--span">SHOP</span>
                        <span class="redirect--span">WEEDINGS</span>
                    </div>
                    <div class="desktop__logoWrapper flexCenter">
                        <span class="logo--span">Flowers's Capital</span>
                    </div>
                    <div class="desktop__spansWrapperRight flexCenter">
                        <span class="redirect--span">BLOG</span>
                        <span class="redirect--span">CONTACT</span>
                    </div>
                    <div class="desktop__icons flexCenter">
                        <img id="shopping" src="../assets/shopping.png" />
                        <img id="user" src="../assets/user.png" />
                    </div>
                </div>
            </div>
            <div :style="{ display: !toggled ? 'block' : 'none'}"
            class="dropdown">
                <div class="dropdown__links">
                    <span>About us</span>
                    <span>Shop</span>
                    <span>Weedings</span>
                    <span>Gallery</span>
                    <span>Blog</span>
                </div>  
                <div class="dropdown__contact">
                    <span>Phone: 212 236-7842</span>
                    <span>contact@flowerscapital.com</span>
                </div>
                <div class="dropdown__socials">
                    <div>
                        <img src="../assets/facebook.png"/>
                        <span>Flowers'Capital NYC</span>
                    </div>
                    <div>
                        <img src="../assets/instagram.png" />
                        <span>@flowers'capitalNYC</span>
                    </div>
                    <div>
                        <img src="../assets/pinterest.png" />
                        <span>Flowers'Capital NYC</span>
                    </div>
                </div>
                

            </div>
        </header>

                
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

    header{
        display: flex;
        justify-content: center;
        padding-top: 15px;
        width: 100%;
        max-width: 5000px;
        height: fit-content;
        margin: 0 auto;
        background: transparent;
        position: absolute;
    }

    .logoText {
        font-size: 35px;
        line-height: 100%;
        letter-spacing: -0.01em;
        color: $gold600;
        text-align: center;
        justify-self: center;
        margin: 0 auto;
    }

    .hamburger {
        position: absolute;
        top: 21px;
        left: 5.128vw;
        display: flex;
        flex-flow: column nowrap;
        width: 5%;
        justify-content: center;
        align-items: center;
        gap: 6px;

        .hamburger--bar{
            height: max(0.5vw, 3px);
            width: clamp(23px, 6vh, 35px);
            color: $gold600;
            border: 1px solid $gold600;
            background: $gold600;
            
        }
    }

    .hamburger__closed{
        position: absolute;
        top: 8px;
        left: 5.128vw;


        .hamburger--x {
            height: max(0.5vw, 3px);
            width: clamp(23px, 6vh, 35px);
            color: $gold600;
            border: 1px solid $gold600;
            background: $gold600;
            
            
    }

    .x-one {
        position: absolute;
        rotate: 45deg;
        top: 21px;
        }
    .x-two {
        position: absolute;
        rotate: -45deg;
        top: 21px;
        }
    }
    


    .desktopHeader {
        display: none;
        width: 95%;
        margin: 0 auto;
        max-width: 2000px;

    }
    .desktopWrapper {
        display: flex;
        position: relative;
        z-index: 999;
        justify-content: space-evenly;
        max-width: 2000px;
        margin: 0 auto;
        
        .desktop__spansWrapperLeft{
            gap: 4.097vw;
        }

        .redirect--span {
            cursor: pointer;
        }

        .redirect--span:after {
            display:block;
            content: '';
            border-bottom: solid 1px $gold600;  
            transform: scaleX(0);  
            transition: transform 250ms ease-in-out;
            }

        .redirect--span:hover:after {
            transform: scaleX(1)
        }

        .desktop__spansWrapperRight{
            gap: 4.236vw;
            padding-right: 2.300vw;
        }

        .desktop__icons {
            gap: 1.806vw;
        }

        .flexCenter{
            display: flex;
            align-items: center;
            
        }

        span {
            font-size: $desktopBody;
            color: $gold600;
        }

        .desktop__logoWrapper {
            justify-content: center;
            text-align: center;
            padding-left: 6.208vw;
            padding-right: 6.139vw;

        }

        .logo--span {
            font-size: $desktopH3;
            line-height: 52.8px;
            letter-spacing: -0.02em;

        }
    }



    .dropdown{
        position: absolute;
        height: 100vh;
        top: 49px;
        font-size: $mobileH4;
        padding-left: 16px;
        background: #F7F8FA;
        width: 100%;
        display: none;
        z-index: 99;
        border-bottom: 1px solid $gold600;
        

        &__links{
            display: flex;
            flex-flow: column nowrap;
            padding-top: 6.571vh;
            
            span {
                padding-bottom: 1.286vh;
            }
        }

        &__contact {
            padding-top: 4.714vh;
            display: flex;
            flex-flow: column nowrap;
            

            span {
                padding-bottom: 2.857vh;
            }

            span + span {
                color: $gold600;
            }
        }

        &__socials {
            padding-top: 3.286vh;

            div {
                display: flex;
                gap: 1.714vh;
                padding-bottom: 2.143vh;
            }
        }
    }


@media screen and (min-width: 1024px) {
    .mobileHeader {
        display: none;
    }

    .desktopHeader {
        display: block;

        .desktop__icons {
            gap: 1.806vw;

            #shopping:hover {
                content: url('../assets/shoppingHover.png');
            }

            #user:hover {
                content: url('../assets/userHover.png');
            }
        }
    }
}

</style>