<script setup>

</script>

<template>
    <div id="gallery" class="preWrapper">
        <div class="instagramWrapper">
            <div class="instagram__Component">
                <div class="component--foto o1-1">
                    <div class="foto foto1"></div>
                </div>
                <div class="component--foto o2-2">
                    <div class="foto foto2"></div>
                </div>
                <div class="component--foto o3-6">
                    <div class="foto foto3"></div>
                </div>
                <div class="component--foto o4-8">
                    <div class="foto foto4"></div>
                </div>
                <div class="component--foto component--foto5 o5-5">
                    <div class="foto foto5"></div>
                </div>
                <div class="component--foto component--foto6 o6-3">
                    <div class="foto foto6"></div>
                </div>
                <div class="component--foto component--foto7 o7-4">
                    <div class="foto foto7"></div>
                </div>
                <div class="component--foto component--foto8 o8-7">
                    <div class="foto foto8"></div>
                </div>
            </div>
            <div class="insagram__linkContainer">
                <p>Follow us on Instagram</p>
                <p>@FLOWERSCAPITALNYC</p>
            </div>
        </div>
    </div>
    
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.preWrapper {
    padding-bottom: 40px;
}

.instagramWrapper {
    position: relative;

    .instagram__Component {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: center;
        gap: 14px;
        max-width: 500px;
        margin: 0 auto;
        


        .component--foto { 
            

            .foto {
                height: 44.103vw;
                width: 44.103vw;
                background-repeat: no-repeat;
                background-size: cover;
                max-height: 230px;
                max-width: 230px;
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
        .component--foto5, .component--foto6, .component--foto7, .component--foto8 {
            display: none;
        }

        .foto5, .foto6, .foto7, .foto8 {
            display: none;
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
        max-width: 420px;
        max-height: 102px;
        background-color: $gold600;
        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
        gap: 5px;

        p {
            color: $white100;
            font-size: $mobileBody;
            text-align: center;
            margin: 0;
        }

        p + p {
            font-size: $mobileBody;
        }

    }
}


@media screen and (min-width: 1024px) {

    .preWrapper {
        padding-bottom: 100px;
    }

    .instagramWrapper {
        max-width:2000px;
        margin: 0 auto;
    
        .instagram__Component {
            gap: 20px;
            margin: 0 15vw 0 15vw;
            max-width: 1600px;

            .o1-1 {
                order: 1;
            }
            .o2-2 {
                order: 2;
            }
            .o3-6 {
                order: 6;
            }
            .o4-8 {
                order: 8;
            }
            .o5-5 {
                order: 5;
            }
            .o6-3 {
                order: 3;
            }
            .o7-4 {
                order: 4;
            }
            .o8-7 {
                order: 7;
            }
            

            .component--foto5, .component--foto6, .component--foto7, .component--foto8 {
                display: block;
            }
    
            .foto5, .foto6, .foto7, .foto8 {
                display: block;
            }
    
    
            .component--foto {
               
                .foto {
                    height: 15.972vw;
                    width: 15.972vw;
                    max-width: none;
                    max-height: none;
                    
                }
    
                .foto5{
                    background-image: url('../assets/instagram5.png');
                    display: block;
                }

                .foto6 {
                    background-image: url('../assets/instagram6.png');
                    display: block;
                }

                .foto7 {
                    background-image: url('../assets/instagram7.png');
                    display: block;
                }

                .foto8 {
                    background-image: url('../assets/instagram8.png');
                    display: block;
                }
            }
    
        }
    
        .insagram__linkContainer {
            width: 40.556vw;
            height: 5.556vw;
            max-width: none;
            max-height: none;
    
            p {
                font-size: 1.597vw;
            }
    
            p + p {
                font-size: 1.25vw;
            }
    
        }
    }
}

@media screen and (min-width: 2000px) {

    .instagramWrapper {
        
        .instagram__Component {
            gap: 20px;
            margin: 0 auto;
            max-width: 1600px;
        }
}
}

</style>