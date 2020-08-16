<template>
  <div class="photo">
      <h2>Usphotoer {{ $route.params.id }}</h2>
    <Photo v-if="photo" :photo="photo" />
    <p v-else>Couldn't find specified photo</p>
  </div>
</template>

<script>
// @ is an alias to /src
import Photo from '@/components/Photo.vue';
import photos from '@/assets/photos';

export default {
  name: 'PhotoView',
  data() {
    return {
      photos,
    };
  },
  components: {
    Photo,
  },
  computed: {
    photo() {
      console.log(this.$route.params.id);
      return this.photos.find((p) => p.id === this.$route.params.id);
    },
  },
};
</script>
