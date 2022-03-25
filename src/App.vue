<template>
  <div id="app">
    <HeaderDisch :data='resulse'></HeaderDisch>
    <MainDisch @x='getData($event)'></MainDisch>
    <FooterDisch/>
    <CardDisch/>
  </div>
</template>

<script>
import HeaderDisch from './components/HeaderDisch.vue'
import MainDisch from './components/MainDisch.vue'
import FooterDisch from './components/FooterDisch.vue'
import CardDisch from './components/CardDisch.vue'

export default {
  name: 'App',
  components: {
    HeaderDisch,
    MainDisch,
    FooterDisch,
    CardDisch
  },
  data () {
    return {
      resulse: []
    }
  },
  methods: {
    getData (datas) {
      datas.forEach((element) => {
        if (!this.resulse.includes(element.genre)) {
          this.resulse.push(element.genre)
        }
      })
      console.log(this.resulse)
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
