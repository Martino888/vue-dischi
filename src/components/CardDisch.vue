<template>
  <div class="col-6 col-md-4 col-lg-3 card-album">
    <img class="img-fluid" :src="cardFor.poster" :alt="cardFor.title">
    <h2>{{cardFor.title}}</h2>
    <b>{{cardFor.author}}</b>
    <b>{{cardFor.year}}</b>
  </div>
</template>

<script>
export default {
  name: 'CardDisch',
  props: {
    cardFor: Object
  }
}
</script>

<style>

</style>
