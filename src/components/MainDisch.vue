<template>
  <main class="bg-black">
    <div class="container">
      <div class="row">
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

<style scoped lang="scss"></style>
