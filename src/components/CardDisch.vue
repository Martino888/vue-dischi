<template>
  <div class="card-album">
    <img :src="cardFor.poster">
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

<style scoped lang="scss">
.card-album{
    width: calc(100% / 5 - 20px);
    min-width: 150px;
    background-color: rgb(48, 58, 69);
    padding: 10px;
    text-align: center;
}

</style>
