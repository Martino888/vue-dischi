<template>
  <div id="app">
    <HeaderDisch/>
    <MainDisch/>
    <FooterDisch/>
  </div>
</template>

<script>
import HeaderDisch from './components/HeaderDisch.vue'
import MainDisch from './components/MainDisch.vue'
import FooterDisch from './components/FooterDisch.vue'

export default {
  name: 'App',
  components: {
    HeaderDisch,
    MainDisch,
    FooterDisch
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
@import "~bootstrap/scss/bootstrap";
</style>
