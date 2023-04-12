<script setup>

</script>

<template>
  <router-view/>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';
@include grotleyFont();
*{
  font-family: 'grotley', sans-serif;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  scroll-behavior: smooth;
}

</style>