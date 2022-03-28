<template>
  <main class="mainbg">
    <div class="container">
      <div class="row col-12">
        <CardDisch v-for="card in arrFilter" :key="card.title" :cardFor="card" />
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
  props: {
    genere: String
  },
  computed: {
    arrFilter () {
      return this.CardDisc.filter(obj => obj.genre.includes(this.genere))
    }
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.CardDisc = response.data.response
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
