<script setup>

</script>

<template>
    <div class="shopWrapper">
        <h2>Shop</h2> 
        <div class="shopInfos">
            <h3>We offer convenient online ordering and delivery services.</h3>
            <p>You can choose from indoor plants, forever green suculents, colorful wreaths and flower crowns, stunning flower boxes, already made bouquets or fresh flowers to make your own composition.</p>
            <p>Discover our offer, select your desired flowers or plants, and we'll take care of the rest.</p>
            <button>Go to our shop</button>
        </div>
    </div>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.shopWrapper {
    position: relative;
    padding-top: $spc72;
    height: 100vh;
    display: flex;

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


</style>