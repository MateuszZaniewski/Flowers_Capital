<script setup>

</script>

<template>
    <section id="weddings" class="weddingComponentMobile">
        <div class="weddingComponentWrapper">
            <h2>Weddings</h2> 
            <div class="weddingInfos">
                <p>Flowers'Capital offers beautiful and personalized wedding floral arrangements. Our experienced team of florists will work with you to bring your vision to life, whether you want a classic, romantic, or modern theme. Our goal is to bring your dream wedding to life with stunning floral arrangements that will leave a lasting impression on you and your guests.</p>
            </div>
        </div>
        <div class="weddingComponentFotoWrapper">
            <div class="fotoWrapper wrap1">
                <div class="foto1"></div>
            </div>
            <div class="fotoWrapper wrap2">
                <div class="foto2"></div>
            </div>
            <div class="fotoWrapper wrap3">
                <div class="foto3"></div>
            </div>
            <div class="fotoWrapper wrap4">
                <div class="foto4"></div>
            </div>
        </div>
    
        <div class="weddingListWrapper">
            <p>We offer a wide range of wedding floral services, including:</p>
            <ul>
                <li>Bridal bouquets</li>
                <li>Bridesmaid bouquets</li>
                <li>Boutonnières</li>
                <li>Flower crowns</li>
                <li>Ceremony décor</li>
                <li>Table arrangements</li>
                <li>Reception centerpieces</li>
                <li>Garlands and arches</li>
            </ul>
            <p>And more! </p>
            <p>Contact us today to schedule a consultation and let us bring the beauty of flowers to your wedding celebration.</p>
            <button>Contact us</button>
            <img class="greyFlower3" src="../assets/greyFlower3.png" />
        </div>
    </section>
    

    <section id="weddings" class="weddingComponentDesktop">
        <div class="weddingComponentWrapper">
            <h2>Weddings</h2> 
            <div class="weddingInfos">
                <p>Flowers'Capital offers beautiful and personalized wedding floral arrangements. Our experienced team of florists will work with you to bring your vision to life, whether you want a classic, romantic, or modern theme. Our goal is to bring your dream wedding to life with stunning floral arrangements that will leave a lasting impression on you and your guests.</p>
            </div>
        </div>

        <div class="weddingFlex">
            <div class="weddingFlex__left">
                <div class="weddingComponentFotoWrapper">
                    <div class="fotoWrapper wrap1">
                        <div class="foto1"></div>
                    </div>
                    <div class="fotoWrapper wrap2">
                        <div class="foto2"></div>
                    </div>
                    <div class="fotoWrapper wrap3">
                        <div class="foto3"></div>
                    </div>
                    <div class="fotoWrapper wrap4">
                        <div class="foto4"></div>
                    </div>
                </div>
            </div>
            <div class="weddingFlex__right">
                <div class="weddingListWrapper">
                    <p>We offer a wide range of wedding floral services, including:</p>
                    <ul>
                        <li>Bridal bouquets</li>
                        <li>Bridesmaid bouquets</li>
                        <li>Boutonnières</li>
                        <li>Flower crowns</li>
                        <li>Ceremony décor</li>
                        <li>Table arrangements</li>
                        <li>Reception centerpieces</li>
                        <li>Garlands and arches</li>
                    </ul>
                    <p>And more! </p>
                    <p class="weddingMore" >Contact us today to schedule a consultation and let us bring the beauty of flowers to your wedding celebration.</p>
                    <button>Contact us</button>
                </div>
            </div>
        </div>
    </section>

</template>

<style scoped lang="scss">

@import '@/assets/_variables.scss';

.weddingComponentMobile {
    .weddingComponentWrapper {
        position: relative;
        display: flex;
        max-width: 2000px;
        margin: 0 auto;
        padding-bottom: 0px;
    
        h2 {
            transform: rotate(180deg);
            white-space: nowrap;
            color: $gold600;
            margin: 0;
            width: fit-content;
            position: absolute;
            z-index: 1;
            top: 0%;
            left: 4%;
            writing-mode: vertical-lr;
            font-size: $mobileH2;
            
          }
    
    
        .weddingInfos {
            width: 80%;
            margin-right: 32px;
            margin-left: clamp(10px, 20vw, 130px);
            padding-bottom: $spc36;
    
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
                color: $white100;
                border: none;
                line-height: 27.6px;
                margin-top: 13px;
            }

            button:hover {
                background: $gold700;
              }
        }
        
    }
    
    .weddingComponentFotoWrapper {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;

        margin-right: 16px;
        padding-bottom: 75px;
    
        .wrap1 {
            display: flex;
            justify-content: flex-end;
            
        }
    
        .wrap2 {
            padding-left: 20px;
            padding-bottom: 20px;
        }
    
        .wrap3 {
            padding-top: 20px;
            display: flex;
            justify-content: flex-end;
        }
    
        .wrap4 {
            padding-left: 20px;
        }
    
    
        .fotoWrapper {
            display: flex;
            width: 50%;
    
    
            .foto1 {
                background-image: url('../assets/foto1.png');
                background-size: cover;
                background-repeat: no-repeat;
                width: 43.333vw;
                height: 55.385vw;
            }
    
            .foto2 {
                background-image: url('../assets/foto2.png');
                background-size: cover;
                background-repeat: no-repeat;
                width: 31.538vw;
                height: 37.436vw;
                align-self: flex-end;
                position: relative;
    
                &:before {
                    content: '';
                    position: absolute;
                    z-index: 1;
                    transform: translateY(-35%);
                    top: -10%;
                    left: 0%;
                    width: 125%;
                    height: 5%;
                    border-top: 2px solid $gold600;
                }
        
            }
    
            .foto3 {
                background-image: url('../assets/foto3.png');
                background-size: cover;
                background-repeat: no-repeat;
                width: 31.538vw;
                height: 37.436vw;
                position: relative;
    
                &:before {
                    content: '';
                    position: absolute;
                    z-index: 1;
                    transform: translateY(-35%);
                    top: 45%;
                    left: -15%;
                    width: 100%;
                    height: 125%;
                    border-left: 2px solid $gold600;
                }
        
                &:after{
                    content: '';
                    position: absolute;
                    z-index: 1;
                    transform: translateY(-50%);
                    top: 110%;
                    left: -25%;
                    width: 125%;
                    height: 5%;
                    border-bottom: 2px solid $gold600;
              
                  }
            }
    
            .foto4 {
                background-image: url('../assets/foto4.png');
                background-size: cover;
                background-repeat: no-repeat;
                width: 43.333vw;
                height: 55.385vw;
            }
        }
    
    }
    
    
    .weddingListWrapper {
        position: relative;
        z-index: 100;
        width: 80%;
        padding-right: 16px;
        margin-left: clamp(10px, 20vw, 130px);
        padding-bottom: 84px;
        font-size: $mobileBody;
    
        p {
            margin: 0;
            padding-bottom: 15px;
        }
    
        ul {
            list-style: none;
            padding-bottom: 15px;
            margin: 0;
    
            li {
                line-height: 27px;
    
                &:before {
                    content: "\2022";
                    color: $gold600;
                    font-size: 25px;
                    display: inline-block; 
                    width: 20px;
                    
    
    
                }
            }
        }
    
    
        button {
            padding: 15px 40px 15px 40px;
            background: $gold600;
            font-size: $mobileBody;
            border-radius: 40px;
            color: $white100;
            border: none;
            line-height: 27.6px;
            margin-top: 13px;
        }

        button:hover {
            background: $gold700;
          }
    
          .greyFlower3 {
            position: absolute;
            top: 30%;
            right: 0;
            z-index: 1;
          }

    }
}

.weddingComponentDesktop {
    display: none;
}

@media screen and (min-width: 1024px) {
    
    .weddingComponentMobile {
        display: none;
    }
    .weddingComponentDesktop {
        display: block;
        padding-bottom: 138px;
        max-width: 2000px;
        margin: 0 auto;
        .weddingComponentWrapper {
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
                z-index: 1;
                top: 0%;
                left: 4%;
                writing-mode: vertical-lr;
                font-size: $mobileH2;
                
              }
        
        
            .weddingInfos {
                width: 80%;
                margin-right: 32px;
                margin-left: clamp(10px, 20vw, 130px);
                padding-bottom: $spc36;
        
                h3 {
                    font-size: $desktopH3;
                    line-height: 34px;
                    color: $black900;
                    margin: 0;
                    padding-bottom: 40px;
        
                }
        
                p {
                    font-size: $desktopH6;
                    line-height: 27.6px;
                    color: $black900;
                    margin: 0;
                    padding-bottom: 20px;
                    width: 60%;
                }
        
                button {
                    padding: 15px 40px 15px 40px;
                    background: $gold600;
                    font-size: $mobileBody;
                    border-radius: 40px;
                    color: $white100;
                    border: none;
                    line-height: 27.6px;
                    margin-top: 13px;
                }

                button:hover {
                    background: $gold700;
                  }
            }
            
        }
    
        .weddingFlex {
            display: flex;
    
    
            .weddingFlex__left {
                width: 50%;
    
                .weddingComponentFotoWrapper {
                    display: flex;
                    flex-wrap: wrap;
                    justify-content: center;
                    margin-left: 16px;
                    margin-right: 16px;
                    padding-bottom: 75px;
                
                    .wrap1 {
                        display: flex;
                        justify-content: flex-end;
                        
                    }
                
                    .wrap2 {
                        padding-left: 20px;
                        padding-bottom: 20px;
                    }
                
                    .wrap3 {
                        padding-top: 20px;
                        display: flex;
                        justify-content: flex-end;
                    }
                
                    .wrap4 {
                        padding-left: 20px;
                    }
                
                
                    .fotoWrapper {
                        display: flex;
                        width: 50%;
                
                
                        .foto1 {
                            background-image: url('../assets/foto1.png');
                            background-size: cover;
                            background-repeat: no-repeat;
                            width: 16.944vw;
                            height: 22.5vw;
                        }
                
                        .foto2 {
                            background-image: url('../assets/foto2.png');
                            background-size: cover;
                            background-repeat: no-repeat;
                            width: 12.5vw;
                            height: 17.639vw;
                            align-self: flex-end;
                            position: relative;
                
                            &:before {
                                content: '';
                                position: absolute;
                                z-index: 1;
                                transform: translateY(-35%);
                                top: -10%;
                                left: 0%;
                                width: 125%;
                                height: 5%;
                                border-top: 2px solid $gold600;
                            }
                    
                        }
                
                        .foto3 {
                            background-image: url('../assets/foto3.png');
                            background-size: cover;
                            background-repeat: no-repeat;
                            width: 12.5vw;
                            height: 17.639vw;
                            position: relative;
                
                            &:before {
                                content: '';
                                position: absolute;
                                z-index: 1;
                                transform: translateY(-35%);
                                top: 45%;
                                left: -15%;
                                width: 100%;
                                height: 125%;
                                border-left: 2px solid $gold600;
                            }
                    
                            &:after{
                                content: '';
                                position: absolute;
                                z-index: 1;
                                transform: translateY(-50%);
                                top: 110%;
                                left: -25%;
                                width: 125%;
                                height: 5%;
                                border-bottom: 2px solid $gold600;
                          
                              }
                        }
                
                        .foto4 {
                            background-image: url('../assets/foto4.png');
                            background-size: cover;
                            background-repeat: no-repeat;
                            width: 16.944vw;
                            height: 22.5vw;
                        }
                    }
                
                }
            }
    
            .weddingFlex__right {
                width: 50%;
    
                .weddingListWrapper {
                    width: 80%;
                    margin: 0 auto;
                    padding-right: 16px;
                    padding-bottom: $spc36;
                    font-size: $desktopH6;
                
                    p {
                        margin: 0;
                        padding-bottom: 23px;
                    }
    
                    .weddingMore {
                        padding-top: 15px;
                        padding-bottom: 25px;
                    }
                
                    ul {
                        list-style: none;
                        padding-bottom: 15px;
                        margin: 0;
                
                        li {
                            line-height: 27px;
                            padding-bottom: 10px;
                
                            &:before {
                                content: "\2022";
                                color: $gold600;
                                font-size: 25px;
                                display: inline-block; 
                                width: 20px;
                                
                
                
                            }
                        }
                    }
                
                
                    button {
                        padding: 15px 40px 15px 40px;
                        background: $gold600;
                        font-size: 25px;
                        border-radius: 40px;
                        color: $white100;
                        border: none;
                        line-height: 27.6px;
                        margin-top: 13px;
                    }

                    button:hover {
                        background: $gold700;
                      }
                
                }
            }
        }
    }

}




</style>