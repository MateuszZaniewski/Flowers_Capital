<script setup>
import { ref, onMounted } from "vue"

const headerWidth = ref(null);
const divWidth = ref(null); 

onMounted(() => {
      divWidth.value = headerWidth.value.clientWidth;
      console.log(divWidth.value)
    });

</script>

<template>
  <section class="aboutUswrapper">
    <div class="aboutUsMain">
      <div class="aboutUsMain__header" ref="headerWidth">
          <h2>About us</h2> 
      </div>
      <div class="aboutUsMain__image">
        <div class="imageDiv"></div>
      </div>
    </div>


    <div class="aboutUsInfos" :style="{marginLeft : divWidth + 'px'}">
      <h3>This is an online flower shop where you can buy guilt-free floral magnificence that doesn’t hurt our planet!</h3>
      <p>Our mission is to provide our customers with the highest quality flowers and plants, along with exceptional customer service.</p>
      <p>All our products are 100% plastic-free, super sustainable and promote zero flower waste.</p>
    </div>
  </section>

  <!-- <div class="AboutUsMobileWrapper">
      <div class="aboutUsNext">
        <div class="doniczkaImage__wrapper">
          <div class="doniczkaImage"></div>
        </div>
        <div class="bukietImage__wrapper">
          <div class="bukietImage"></div>
        </div>
      </div>
    </div> -->

  <!-- <div class="aboutUsInfos" :style="{marginLeft : divWidth + 'px'}">
      <p>We pride ourselves on the wide variety of fresh flowers and plants that we offer.</p>
      <p>Whether you're looking for a beautiful bouquet of roses for a special occasion, or a lush green plant to liven up your home or office, we have something to suit everyone's taste and budget.</p>
      <button>Learn more</button>
    </div> -->

    <div class="AboutUsDesktopWrapper">
      <div class="aboutUsLeft">
        <div class="aboutUsInfos">
          <p>We pride ourselves on the wide variety of fresh flowers and plants that we offer.</p>
          <p>Whether you're looking for a beautiful bouquet of roses for a special occasion, or a lush green plant to liven up your home or office, we have something to suit everyone's taste and budget.</p>
          <button>Learn more</button>
        </div>
      </div>
      <div class="aboutUsRight">
        <div class="cactusImageWrapper">
          <div class="cactusImage"></div>
        </div>
        <div class="bukietImageWrapper">
          <div class="bukietImage"></div>
        </div>
        <div class="flowersImageWrapper">
          <div class="flowersImage"></div>
        </div>
        <div class="doniczkaImageWrapper">
          <div class="doniczkaImage"></div>
        </div>
      </div>
    </div>

</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.aboutUswrapper {
  margin-top: 45px;
  max-width: 800px;
  z-index: 1;


  .aboutUsMain {

    display: flex;

    &__image {
      height: auto;
      width: auto;
      position: relative;
      padding-left: 20px;
      padding-bottom: 20px;

      .imageDiv {
        height: 76.923vw;
        width: 55.897vw;
        background-image: url("../assets/aboutImageHighRes.png");
        background-size: cover;
        background-repeat: no-repeat;
      }
    } 

    &__image:before{
      content: '';
      position: absolute;
      z-index: 1;
      transform: translateY(-35%);
      top: 45%;
      left: 0;
      width: 90%;
      height: 90%;
      border-left: 2px solid $gold600;

    }

    &__image:after{
      content: '';
      position: absolute;
      z-index: 1;
      transform: translateY(-50%);
      top: 50%;
      left: -5%;
      width: 110%;
      height: 100%;
      border-bottom: 2px solid $gold600;

    }
  
    &__header{

      width: 20%;
      max-width: 130px;
      position: relative;
      

      h2 {
        transform: rotate(180deg);
        white-space: nowrap;
        color: $gold600;
        margin: 0;
        width: fit-content;
        position: absolute;
        z-index: 1;
        top: 14%;
        right: 10px;
        writing-mode: vertical-rl;
        font-size: $mobileH2;
        
      }
    }

  }
  
}


.aboutUsInfos{
  margin-right: 32px;
  position: relative;
  padding-bottom: $spc32;

  h3 {
    margin-top: 64px;
    color: $gold600;
    line-height: 33.6px;
    font-size: $mobileH3;
    letter-spacing: -1px;
    padding-bottom: $spc32;
  }

  p {
    line-height: 27px;
    font-size: $mobileBody;
    padding-bottom: 21px;
  }

  button {
    padding: 15px 40px 15px 40px;
    background: $gold600;
    font-size: $mobileH4;
    border-radius: 40px;
    color: $white100;
    border: none;
    line-height: 27.6px;
  }
}

.AboutUsMobileWrapper {
  display: flex;
  padding-bottom: 30px;
  width: 90%;
  margin: 0 auto;
  
}

.aboutUsNext {

  position: relative;
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-around;
  gap: 25px;
  align-items: flex-end;
  width: 90%;
  margin: 0 auto;

  .doniczkaImage__wrapper{

    height: auto;
    width: auto;
    position: relative;
    padding-left: 20px;
    padding-bottom: 20px;
    display: flex;
    justify-content: center;

    &:before{
      content: '';
      position: absolute;
      z-index: 1;
      transform: translateY(-35%);
      top: 45%;
      left: 0;
      width: 90%;
      height: 100%;
      border-left: 2px solid $gold600;
  
    }

    &:after{
      content: '';
      position: absolute;
      z-index: 1;
      transform: translateY(-50%);
      top: 50%;
      left: -5%;
      width: 105%;
      height: 100%;
      border-bottom: 2px solid $gold600;
  
    }

  }
  
  .doniczkaImage {
    height: 35.897vw;
    width: 35.897vw;
    background-image: url('../assets/doniczkaHighRes.png');
    background-repeat: no-repeat;
    background-size: cover; 

  }

}


.bukietImage__wrapper {

  width: 100%;
  display: flex;
  justify-content: center;

  .bukietImage {
    height: 68.718vw;
    width: 43.333vw;
    background-image: url('../assets/bukietHighRes.png');
    background-repeat: no-repeat;
    background-size: cover;
    border-radius: 200px 200px 0 0;
  }

}




.AboutUsDesktopWrapper {
  padding-top: 100px;
  display: flex;
  width: 90%;
  margin: 0 auto;
  justify-content: space-around;

  .aboutUsLeft {
    width: 40%;

    p {
      font-size: $desktopH6;
    }

    button {
      font-size: 28px;
    }
  }

  .aboutUsRight{
    display: flex;
    flex-wrap: wrap;
    width: 60%;
    justify-content: center;

    .cactusImage {
      background-image: url('../assets/cactusHighRes.png');
      height: 13.889vw;
      width: 15.278vw;
      background-repeat: no-repeat;
      background-size: cover;
    }
    .bukietImage {
      background-image: url('../assets/bukietHighRes.png');
      height: 26.042vw;
      width: 17.361vw;
      background-repeat: no-repeat;
      background-size: cover;
      border-radius: 200px 200px 0 0;
    }
    .flowersImage {
      background-image: url('../assets/flowersHighRes.png');
      height: 19.444vw;
      width: 25.903vw;
      background-repeat: no-repeat;
      background-size: cover;
    }
    .doniczkaImage {
      background-image: url('../assets/doniczkaHighRes.png');
      height: 15.278vw;
      width: 15.278vw;
      background-repeat: no-repeat;
      background-size: cover;
    }

    .cactusImageWrapper {
      display: flex;
      align-items: flex-end;
      justify-content: flex-end;
      position: relative;
      padding-right: 10px;
      padding-bottom: 20px;
      width: 50%;

      &:before {
        content: '';
        position: absolute;
        z-index: 1;
        transform: translateY(-35%);
        top: 37%;
        left: 16%;
        width: 80%;
        height: 10%;
        border-top: 2px solid $gold600;
      }
    }

    .bukietImageWrapper {
      display: flex;
      align-items: flex-end;
      padding-left: 10px;
      padding-bottom: 0;
      width: 50%;
    }

    .flowersImageWrapper {
      display: flex;
      align-items: flex-start;
      justify-content: flex-start;
      width: 50%;
    }

    .doniczkaImageWrapper {
      position: relative;
      display: flex;
      justify-content: flex-start;
      width: 50%;
      padding-top: 20px;
      padding-left: 10px;

      &:before {
        content: '';
        position: absolute;
        z-index: 1;
        transform: translateY(50%);
        top: -35%;
        left: -60%;
        width: 125%;
        height: 90%;
        border-right: 2px solid $gold600;
      }

      &:after {
        content: '';
        position: absolute;
        z-index: 1;
        transform: translateY(-35%);
        top: 75%;
        left: 3%;
        width: 70%;
        height: 30%;
        border-bottom: 2px solid $gold600;
      }
    }
  }
}






@media screen and (min-width: 800px) and (max-width: 1023px) {
  .aboutUswrapper {
    width: 100%;
    max-width: 1600px;
    margin: 0 auto;
}

.imageDiv {
  width: 100%;
  height: 100%;
  background-image: url("../assets/aboutImageHighRes.png");
  background-size: contain;
  background-repeat: no-repeat;
}
}


@media screen and (min-width: 1024px) {
  
  .aboutUswrapper {
    display: flex;
    justify-content: space-between;
    max-width: 1400px;
    margin: 50px auto 0 auto;

    .aboutUsMain {
      width: 60%;
      max-height: 700px;
      max-width: 1000px;

      &__image {
        height: auto;
        width: auto;
        position: relative;
        padding-left: 20px;
        padding-bottom: 20px;
  
        .imageDiv {
          height: 660px;
          width: 420px;
          background-image: url("../assets/aboutImageHighRes.png");
          background-size: cover;
          background-repeat: no-repeat;
        }
      }
      
      &__header{

        width: 20%;
        max-width: 130px;
        position: relative;
        
  
        h2 {
          transform: rotate(180deg);
          white-space: nowrap;
          color: $gold600;
          margin: 0;
          width: fit-content;
          position: absolute;
          z-index: 1;
          top: 14%;
          right: 10px;
          writing-mode: vertical-rl;
          font-size: $desktopH3;
          
        }
      }
    }

    .aboutUsInfos{
      margin: 60px 100px 0 20px;
      width: 45%;
    
      h3 {
        color: $gold600;
        line-height: 33.6px;
        font-size: $desktopH4;
        letter-spacing: -1px;
        padding-bottom: $spc32;
        width: 100%;
      }
    
      p {
        line-height: 27px;
        font-size: $desktopH6;
        padding-bottom: 21px;
        width: 80%;
      }
    
      &__leaf {
        position: relative;
    
        img {
          position: absolute;
          z-index: 1;
          left: 0;
        }
      }
    }

  }

  

}

</style>