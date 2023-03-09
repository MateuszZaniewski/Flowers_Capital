<script setup>

</script>

<template>
  <section class="aboutUswrapper">
    <div class="aboutUsMain">
      <div class="aboutUsMain__header"><h2>About us</h2></div>
      <div class="aboutUsMain__image"><img src="../assets/aboutImage.png"/></div>
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
  padding-top: 45px;

  .aboutUsMain{
    display: flex;

    &__header {
      width: 10%;
      display: flex;
      flex-flow: column;
      justify-content: flex-start;
      position: relative;

      h2{
        transform: rotate(270deg);
        width: fit-content;
        margin: 0;
        white-space: nowrap;
        position: absolute;
        top: 104px;
        left: -35px;
        font-size: $mobileH2;
        color: $gold600;
      }
    }

    &__image {
      width: 85%;

      img {
        width: 100%;
        height: 100%;
      }
    }
  }
}

.aboutUsInfos{
  margin: 0 16px 0 80px;

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