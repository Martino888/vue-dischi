<template>
  <header class="nav  d-flex justify-content-between">
    <img class="logo" src="@/assets/img/spotify_logo.png" alt="">
    <select class="select"  v-model="userSelect" @change="$emit('x', userSelect)">
      <option value="">all</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
  </header>
</template>

<script>
export default {
  name: 'HeaderDisch',
  data () {
    return {
      userSelect: ''
    }
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

.select{
  width: 150px;
  margin: 10px 50px;
  border-radius:10px;
}

</style>
