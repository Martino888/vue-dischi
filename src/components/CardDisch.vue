<template>
  <div class="card-album">
    <img :src='cardFor.poster'>
    <h4 class="text-white">{{cardFor.title}}</h4>
    <div class="fw-bold text-secondary">{{cardFor.author}}</div>
    <div class="fw-bold text-secondary">{{cardFor.year}}</div>
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
    background-color: rgb(63, 77, 92);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
    margin-top: 10px;
}

img {
  width: 140px;
  height: 140px;
}

</style>
