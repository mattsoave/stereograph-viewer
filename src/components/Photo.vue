<template>
  <div class="stereograph">
      <img v-if="photo" :src="`/photos/${photo.photos.left}`" />
      <img v-if="photo" :src="`/photos/${photo.photos.right}`" />
  </div>
</template>

<script>
export default {
  name: 'Photo',
  props: {
    photo: {
      type: Object,
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.stereograph {

  img {
    &:first-child {
      margin-right: 10px;
    }
    width: 300px;
  }
}
</style>
