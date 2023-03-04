<script setup>

</script>

<template>
    <main>
        <div class="heroImageWrapper">
            <img src="../assets/piwoniaMobile.png">
        </div>
    </main>
    
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

main {
    background: $white100;
    overflow: hidden;
}

.heroImageWrapper {

    img {
        height: 100%;
        width: 100%;
        rotate: -110deg;
        overflow: hidden;
        
    }
    
}

</style>

