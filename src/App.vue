<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="photo of photos">
        <img :src="photo.url" :alt="photo.titulo">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  created() {
    this.$http.get('http://localhost:3000/v1/fotoss')
      .then(response => response.json())
      .then(photos => this.photos = photos)
      .catch(error => console.log(error.data));
  },

  data() {
    return {
      title: 'Alurapic - Vue.js',
      photos: [
        // {
        //   url: 'https://cdn.pixabay.com/photo/2017/10/04/18/11/road-2817102_960_720.jpg',
        //   titulo: 'Horizon'
        // },
        // {
        //   url: 'https://cdn.pixabay.com/photo/2019/10/19/12/21/hot-air-balloons-4561267_960_720.jpg',
        //   titulo: 'Ballon'
        // }
      ]
    }
  }
}
</script>

<style>

</style>
