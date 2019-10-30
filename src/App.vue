<template>
  <div>
    <h1>{{ title }}</h1>
    <img :src="photo.imgUrl" :alt="photo.title">
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Alurapic - Vue.js',
      photo: {
        imgUrl: 'https://cdn.pixabay.com/photo/2017/10/04/18/11/road-2817102_960_720.jpg',
        title: 'Horizon'
      }
    }
  }
}
</script>

<style>
</style>
