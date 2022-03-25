<template>
  <main class="mainbg">
    <div class="container">
      <div class="row col-12">
        <CardDisch v-for="card in CardDisc" :key="card.title" :cardFor="card" />
      </div>
    </div>
  </main>
</template>

<script>
import CardDisch from '@/components/CardDisch.vue'
import axios from 'axios'
export default {
  nome: 'MainDisch',
  data () {
    return {
      CardDisc: []
    }
  },
  components: {
    CardDisch
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res) => {
      this.CardDisc = res.data.response
    })
    this.$emit('x', this.CardDisc)
  }
}
</script>

<style scoped lang="scss">
.container {
  justify-content: center;
}

.row {
  padding:90px;
}

.mainbg{
  background-color:rgb(46, 58, 73);
}
</style>
