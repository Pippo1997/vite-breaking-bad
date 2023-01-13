<script>
export default {
  props:{
    characters: Object
  }
}
</script>

<template lang="">
  <div class="character text-center">
    <img class="img-fluid" :src="characters.card_images[0].image_url_small" :alt="characters.name">
    <h4>{{ characters.name }}</h4>
  </div>
</template>

<style lang="scss" scoped>
  
</style>