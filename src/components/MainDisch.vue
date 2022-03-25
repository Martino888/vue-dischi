<template>
  <main class="bg-black">
    <div class="container">
      <div class="row">
        <CardDisch v-for="card in CardDisch" :key="card.poster" :cardFor="card" />
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
      CardDisch: [

      ]
    }
  },
  components: {
    CardDisch
  },
  create () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
        this.CardDisch = response.data.response
        console.log(CardDisch)
      })
  }
}
</script>

<style scoped lang="scss"></style>
