<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="photo of photos">
        <img :src="photo.imgUrl" :alt="photo.title">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Alurapic - Vue.js',
      photos: [
        {
          imgUrl: 'https://cdn.pixabay.com/photo/2017/10/04/18/11/road-2817102_960_720.jpg',
          title: 'Horizon'
        },
        {
          imgUrl: 'https://cdn.pixabay.com/photo/2019/10/19/12/21/hot-air-balloons-4561267_960_720.jpg',
          title: 'Ballon'
        }
      ]
    }
  }
}
</script>

<style>

</style>
