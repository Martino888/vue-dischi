<template>
  <div id="app">
    <HeaderDisch @x="selectGenere"></HeaderDisch>
    <MainDisch :genere = genere></MainDisch>
    <FooterDisch/>
    <CardDisch/>
  </div>
</template>

<script>
import HeaderDisch from './components/HeaderDisch.vue'
import MainDisch from './components/MainDisch.vue'
import CardDisch from './components/CardDisch.vue'

export default {
  name: 'App',
  components: {
    HeaderDisch,
    MainDisch,
    CardDisch
  },
  data () {
    return {
      genere: ''
    }
  },
  methods: {
    selectGenere (genre) {
      this.genere = genre
    }
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
