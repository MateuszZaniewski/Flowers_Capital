<script setup>

</script>

<template>
    <div class="instagramWrapper">
        <div class="instagram__Component">
            <div class="component--foto">
                <div class="foto foto1"></div>
            </div>
            <div class="component--foto">
                <div class="foto foto2"></div>
            </div>
            <div class="component--foto">
                <div class="foto foto3"></div>
            </div>
            <div class="component--foto">
                <div class="foto foto4"></div>
            </div>
        </div>
        <div class="insagram__linkContainer">
            <p>Follow us on Instagram</p>
            <p>@FLOWERSCAPITALNYC</p>
        </div>
    </div>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.instagramWrapper {
    position: relative;

    .instagram__Component {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        gap: 14px;
        


        .component--foto {

            

            .foto {
                height: 44.103vw;
                width: 44.103vw;
                background-repeat: no-repeat;
                background-size: cover;
            }

            .foto1 {
                background-image: url('../assets/instagram1.png');
            }

            .foto2 {
                background-image: url('../assets/instagram2.png');
            }

            .foto3 {
                background-image: url('../assets/instagram3.png');
            }

            .foto4{
                background-image: url('../assets/instagram4.png');
            }
        }

    }

    .insagram__linkContainer {
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        margin: auto;
        width: 83.846vw;
        height: 20.513vw;
        background-color: $gold600;
        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
        gap: 5px;

        p {
            color: $white100;
            font-size: $mobileH4;
            text-align: center;
            margin: 0;
        }

        p + p {
            font-size: $mobileBody;
        }

    }
}

</style>