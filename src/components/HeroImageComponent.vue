<script setup>

</script>

<template>
    <main>
        <div class="heroImageWrapper">
            <div>
                <img src="../assets/piwoniaMobile.png" />
            </div>
            
        </div>
        <h1>
            Welcome to our world of flowers
        </h1>
        <div class="downWrapper">
            <img src="../assets/downPage.png" />
        </div>
    </main>
    
</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

main {
    background: $white100;

    h1 {
        font-size: $mobileH1;
        line-height: 52.8px;
        letter-spacing: -2%;
        text-align: center;
        color: $gold600;
        padding-top: $spc32;
    }
}

.heroImageWrapper {
    display: flex;
    justify-content: flex-end;
    align-items: center;

    img {
        max-height: 100%;
        max-width: 100%;
        object-fit: cover;
        max-height: 900px;
        margin: 0;
    }
}

.downWrapper{
    display: flex;
    justify-content: center;
    padding-top: $spc72;
}

@media screen and (min-width: 1200px) {

    main {
        background: $white100;
    
        h1 {
            font-size: $desktopH1;
            line-height: 85.14px;
            text-align: center;
            color: $gold600;
            padding-top: $spc32;
        }
    }

    .heroImageWrapper {
        display: flex;
        justify-content: flex-end;
        align-items: center;
    
        img {
            max-height: 100%;
            max-width: 100%;
            object-fit: cover;
            max-height: 900px;
            margin: 0;
        }
    }
}

</style>

