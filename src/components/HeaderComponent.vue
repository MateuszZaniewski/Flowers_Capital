<script setup>
console.log('hello script setup')
</script>

<template>
    <header>
        <div class="hamburger--Menu">
                    
        </div>
    </header>
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

.hamburger--Menu {
    margin-top: 1.5rem;
    width: 30px;
    height: 2px;
    background: black;
    position: relative;
    

    &::after {
        content: '';
        position: absolute;
        top: -8px;
        width: 30px;
        height: 2px;
        background: inherit;
        

    }

    &::before {
        content: '';
        position: absolute;
        top: 8px;
        width: 30px;
        height: 2px;
        background: inherit;
        

    }

    &.open {
        transform: rotate(720deg);
        background-color: transparent;
        

        &::before {
            transform: rotate(45deg) translate(-2px, -6px);
            background-color: black;
        }

        &::after {
            width: 28px;
            transform: rotate(-45deg) translate(-5px, 9px);
            background-color: black;
        }
}



}


</style>