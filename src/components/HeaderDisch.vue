<template>
  <div class="nav  d-flex justify-content-between">
    <img class="logo" src="@/assets/img/spotify_logo.png" alt="">
    <select class="">
      <option value="all">all</option>
      <option v-for="genere in data" :value="genere" :key="genere">{{ genere }}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'HeaderDisch',
  props: {
    data: []

  }
}
</script>

<style scoped lang="scss">
.nav{
  max-width: 100%;
  background-color: rgb(63, 77, 92);
}
.logo{
  width: 69px;
}

</style>
