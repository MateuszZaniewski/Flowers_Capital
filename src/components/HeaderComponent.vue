<script setup>
import { ref } from 'vue';

console.log('hello script setup')

let toggled = ref(true)

function isToggled() {
    toggled.value = !toggled.value
    console.log(toggled.value)
}



const windowWidth = window.innerWidth

</script>

<template>
        <header>
            <div class="mobileHeader" v-if="windowWidth < 900">
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
            <div class="desktopHeader" v-if="windowWidth > 901">
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
                        <img src="../assets/shopping.png" />
                        <img src="../assets/user.png" />
                    </div>
                </div>
            </div>
        </header>

                
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

    #trans {
        background: transparent;
    }

    header{
        display: flex;
        justify-content: center;
        padding-top: 15px;
        width: 100%;
        background: $white100;
        height: fit-content;
    }

    .logoText {
        font-size: 35px;
        line-height: 100%;
        letter-spacing: -0.01em;
        color: $gold600;
        text-align: center;
        justify-self: center;
        margin: 0;
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
        width: 95%;
        margin: 0 auto;
    }
    .desktopWrapper {
        display: flex;
        justify-content: space-evenly;
        
        .desktop__spansWrapperLeft{
            gap: 4.097vw;
        }

        .desktop__spansWrapperRight{
            gap: 4.236vw;
            padding-right: 2.444vw;
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
            padding-left: 11.208vw;
            padding-right: 11.139vw;

        }

        .logo--span {
            font-size: $desktopH3;
            line-height: 52.8px;
            letter-spacing: -0.02em;

        }
    }

</style>