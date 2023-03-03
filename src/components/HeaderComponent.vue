<script setup>
import { ref } from 'vue';

console.log('hello script setup')

let toggled = ref(false)

function isToggled() {
    toggled.value = !toggled.value
    console.log(toggled)
}
</script>

<template>
        <header>
            <div class="hamburger">
                <span class="hamburger--bar"></span>
                <span class="hamburger--bar"></span>
                <span class="hamburger--bar"></span>
            </div>
            <p class="logoText">Flower's Capital</p>
        </header>
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

    header{
        display: flex;
        justify-content: center;
        padding-top: 15px;
    }

    .logoText {
        font-size: 35px;
        line-height: 100%;
        letter-spacing: -0.01em;
        color: $gold600;
        text-align: center;
        margin: 0;
        width: 80%;
        justify-self: center;
    }

    .hamburger {
        position: absolute;
        top: 21px;
        left: 5.128vw;
        display: flex;
        flex-flow: column nowrap;
        width: 10%;
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

</style>