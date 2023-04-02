

<script setup>

import HeaderComponent from '../components/HeaderComponent.vue';
import HeroImageComponent from '../components/HeroImageComponent.vue';
import AboutUsComponent from '../components/AboutUsComponent.vue';
import ShopComponent from '../components/ShopComponent.vue';
import WeddingAdvertiserComponent from '../components/WeddingAdvertiserComponent.vue';
import WeddingComponent from '../components/WeddingComponent.vue';
import HowWeDoItComponent from '../components/HowWeDoItComponent.vue';
import BlogComponent from '../components/BlogComponent.vue';
import InstagramComponent from '../components/InstagramComponent.vue';
import FooterComponent from '../components/FooterComponent.vue';


</script>

<template>
  <div class="HomeViewwrapper">
    <HeaderComponent/>
    <HeroImageComponent/>
    <AboutUsComponent/>
    <ShopComponent/>
    <WeddingAdvertiserComponent/>
    <WeddingComponent/>
    <HowWeDoItComponent/>
    <BlogComponent/>
    <InstagramComponent/>
    <FooterComponent/>
  </div>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';

.HomeViewwrapper {
  background: $white100;
}

</style>
