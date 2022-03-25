<template>
  <main class="mainbg">
    <div class="container">
      <div class="row col-12">
        <CardDisch v-for="card in CardDisc" :key="card.poster" :cardFor="card" />
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
      CardDisc: null
    }
  },
  components: {
    CardDisch
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((res) => {
        this.CardDisc = res.data.response
        console.log(res)
      })
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
