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
                <span class="addressTittle">ADDRESS</span>
                <span class="addressRest">54 Orchid St</span>
                <span class="addressRest">New York, NY 10032</span>
            </div>
            <div class="footer--contact">
                <span class="contactTittle">CONTACT US</span>
                <span class="contactRest">Phone: (212) 236-7842</span>
                <span class="contactRest">contact@flowerscapital.com</span>
            </div>
            <div class="footer--follow">
                <span class="followTittle">FOLLOW US</span>
                <div class="follow--socials">
                    <img src="facebook" />
                    <img src="instagram" />
                    <img src="pinterest" />
                </div>
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
        margin-left: 14px;
        padding-bottom: 40px;
        

        p {
           margin: 0;
           width: fit-content;
           line-height: 55px;
        }
        
    }

    .footer__addressWrapper {
        display: flex;
        flex-flow: column nowrap;
        gap: 40px;

        .footer--address {
            display: flex;
            flex-flow: column nowrap;
            justify-content: center;
            align-items: center;

            .addressTittle {
                font-size: $mobileH4;
                padding-bottom: 8px;
            }
        }
    }
}

</style>