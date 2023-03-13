<script setup>

</script>

<template>
  <section class="aboutUswrapper">


    <div class="aboutUsMain">
      <div class="aboutUsMain__header">
        
          <h2>About us</h2> 
        
      </div>
      <div class="aboutUsMain__image">
        <div>
          <img src="../assets/aboutImageHighRes.png">
        </div>
      </div>
    </div>


    <div class="aboutUsInfos">
      <h3>This is an online flower shop where you can buy guilt-free floral magnificence that doesn’t hurt our planet!</h3>
      <p>Our mission is to provide our customers with the highest quality flowers and plants, along with exceptional customer service.</p>
      <div class="aboutUsInfos__leaf">
        <p>All our products are 100% plastic-free, super sustainable and promote zero flower waste.</p>
        <img src="../assets/leaf.png">
      </div>

    </div>
  </section>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.aboutUswrapper {
  margin-top: 45px;
  max-width: 800px;


  .aboutUsMain {

    display: flex;

    &__image {
      width: 80%;
      position: relative;

      div {
        width: 80%;
        height: 100%;

        img{
          height: 100%;
          width: 100%;
          padding-left: 8%;
          padding-bottom: 8%;
        }
      }
    } 

    &__image:before{
      content: '';
      position: absolute;
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
      transform: translateY(-50%);
      top: 50%;
      left: -5%;
      width: 90%;
      height: 100%;
      border-bottom: 2px solid $gold600;

    }
  
    &__header{

      width: 20%;
      position: relative;
      

      h2 {
        transform: rotate(270deg);
        white-space: nowrap;
        color: $gold600;
        margin: 0;
        width: fit-content;
        position: absolute;
        top: 23%;
        right: 0;
        left: 0;
        
      }
    }

  }
  
}


.aboutUsInfos{
  margin: 60px 16px 0 88px;

  h3 {
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

  &__leaf {
    position: relative;

    img {
      position: absolute;
      left: 0;
    }
  }
}


</style>