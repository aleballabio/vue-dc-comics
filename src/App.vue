<template>
    <div id="app">
      <HeaderDC />
      <MainDC />
      <FooterDC />
  </div>
</template>

<script>
import HeaderDC from './components/Header.vue';
import MainDC from './components/Main.vue';
import FooterDC from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    HeaderDC,
    MainDC,
    FooterDC,
  }
}
</script>



<style lang="scss">

@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700;1,900&display=swap');;

  #app {
    font-family: 'Source Sans Pro', sans-serif;
}
</style>
