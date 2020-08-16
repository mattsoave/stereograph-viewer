<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <ul class="photo-thumbnails">
      <li v-for="photo in photos" :key="photo.id">
        <router-link :to="`/photo/${photo.id}`">
          <img :src="`/photos/${photo.photos.left}`" />
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src
import photos from '@/assets/photos';

export default {
  name: 'Home',
  data() {
    return {
      photos,
    };
  },
  components: {
  },
};
</script>

<style scoped lang="scss">
  .photo-thumbnails {
    li {
      display: inline-block;
      margin-right: 5px;
    }
    img {
      width: 100px;
    }
  }
</style>
