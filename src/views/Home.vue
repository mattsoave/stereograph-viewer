<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <ul>
      <li v-for="photo in photos" :key="photo.photos.left">{{photo.photos}}</li>
    </ul>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import photos from '@/assets/photos';

export default {
  name: 'Home',
  data() {
    return {
      photos,
    };
  },
  components: {
    HelloWorld,
  },
};
</script>
