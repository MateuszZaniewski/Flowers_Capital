<script setup>

</script>

<template>
    <div class="footerComponentWrapper">
        <div class="footer__logo">
            <p>Flowers'</p>
            <p>Capital</p>
        </div>
        <div class="footer__addressWrapper">
            <div class="footer--address">
                <span class="footer--tittle">ADDRESS</span>
                <span class="addressRest">54 Orchid St</span>
                <span class="addressRest">New York, NY 10032</span>
            </div>
            <div class="footer--contact">
                <span class="footer--tittle">CONTACT US</span>
                <span class="addressRest">Phone: (212) 236-7842</span>
                <span class="addressRest">contact@flowerscapital.com</span>
            </div>
            <div class="footer--follow">
                <span class="footer--tittle">FOLLOW US</span>
                <div class="follow--socials">
                    <img id="facebook" src="../assets/facebook.png" />
                    <img id="instagram" src="../assets/instagram.png" />
                    <img id="pinterest" src="../assets/pinterest.png" />
                </div>
            </div>
        </div>
        <div class="footer__linksWrapper">
            <div class="footer__links">
                <a>ABOUT US</a>
                <a>GALLERY</a>
                <a>SHOP</a>
                <a>BLOG</a>
                <a>WEDDINGS</a>
            </div>
            <div class="footer__image">
                <div class="image"></div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.footerComponentWrapper {
    border-top: 2px solid $gold600;
    color: $gold600;

    .footer__logo {
        display: flex;
        flex-flow: column nowrap;
        font-size: $mobileH1;
        padding-left: 14px;
        padding-bottom: 40px;
        padding-top: 36px;
        max-width: 600px;
        margin: 0 auto;
        

        p {
           margin: 0;
           width: fit-content;
           line-height: 55px;
        }
        
    }

    .footer--tittle {
                font-size: $mobileH4;
                padding-bottom: 4px;
            }

    .footer__addressWrapper {
        display: flex;
        flex-flow: column nowrap;
        gap: 40px;

        .addressRest {
            font-size: $mobileBody;
            padding-top: 4px;
            line-height: 27px;
        }

        .footer--address {
            display: flex;
            flex-flow: column nowrap;
            justify-content: center;
            align-items: center;

        }

        .footer--contact {
            display: flex;
            flex-flow: column nowrap;
            justify-content: center;
            align-items: center;
        }

        .footer--follow {
            display: flex;
            flex-flow: column nowrap;
            justify-content: center;
            align-items: center;

            .follow--socials {
                display: flex;
                padding-top: 1vh;
                gap: 20px;

                #facebook:hover{
                    content: url('../assets/facebookHover.png');
                }

                #instagram:hover{
                    content: url('../assets/instagramHover.png');
                }

                #pinterest:hover{
                    content: url('../assets/pinterestHover.png');
                }
            }
        }
    }

    .footer__linksWrapper {
        margin: 0 auto;
        padding-top: 40px;
        position: relative;
        

        .footer__links {
            display: flex;
            flex-flow: row wrap;
            padding-left: 20px;
            max-width: 600px;
            margin: 0 auto;
            

            a {
                width: 50%;
                padding-bottom: 20px;
                font-size: $mobileBody;
                
            }
        }

        .footer__image {
            position: absolute;
            bottom: 0;
            right: 0;
            height: 160px;
            width: 100px;
            padding: 0;
            margin: 0;

            .image {
                height: 100%;
                width: 100%;
                background-image: url('../assets/footerImage.png');
                background-repeat: no-repeat;
                background-size: cover;
            }
        }
    }
}


@media screen and (min-width: 1024px) {
    
    .footerComponentWrapper {
        max-width: 2000px;
        margin: 0 auto;

        .footer__logo {
            padding-left: 40px;
            padding-bottom: 40px;
            max-width: auto;
            margin: 0;
            font-size: $desktopH3;
            
    
            p {
               margin: 0;
               width: fit-content;
               line-height: 55px;
            }
            
        }


        .footer__addressWrapper {
            display: flex;
            flex-flow: row nowrap;
            align-items: flex-start;
            gap: 0px;
            justify-content: center;
            padding-bottom: 5.83vw;

            .addressRest {
                font-size: $desktopH6;
                padding-top: 4px;
                line-height: 27px;
            }

            .footer--address {
                order: 1;
            }

            .footer--follow {
                order: 2;
                padding-left: 8.125vw;
                padding-right: 5.625vw;
            }

            .footer--tittle {
                font-size: $desktopH5;
                padding-bottom: 25px;
            }


            .footer--contact {
                order: 3;
                display: flex;
                flex-flow: column nowrap;
                justify-content: center;
                align-items: center;
                
            }
        }

        .footer__linksWrapper {
            margin: 0 auto;
            padding-top: 0px;
            position: relative;

                &:before {
                    content: '';
                    position: absolute;
                    z-index: 1;
                    transform: translateY(-35%);
                    top: 0%;
                    width: 100%;
                    border-top: 2px solid $gold600;
                }
            
    
            .footer__links {
                display: flex;
                flex-flow: row nowrap;
                justify-content: center;
                gap: 6.111vw;
                padding-left: 0;
                padding-top: 13px;
                padding-bottom: 13px;
                max-width: 800px;
                
    
                a {
                    width: fit-content;
                    padding-bottom: 0px;
                    font-size: $mobileBody;
                    cursor: pointer;
                }

                a:after {
                    display:block;
                    content: '';
                    border-bottom: solid 1px $gold600;  
                    transform: scaleX(0);  
                    transition: transform 250ms ease-in-out;
                    }
        
                a:hover:after {
                    transform: scaleX(1)
                }

            }
    
            .footer__image {
                position: absolute;
                bottom: 0;
                right: 0;
                height: 23.611vw;
                width: 12.5vw;
                padding: 0;
                margin: 0;
                z-index: 0;
    
                .image {
                    height: 100%;
                    width: 100%;
                    background-image: url('../assets/footerDesktop.png');
                    background-repeat: no-repeat;
                    background-size: cover;
                }
            }
        }

    }

    
}
</style>