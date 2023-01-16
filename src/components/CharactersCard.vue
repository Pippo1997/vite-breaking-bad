<script>
export default {
  props:{
    characters: Object
  }
}
</script>

<template lang="">
  <div class="character text-center">
    <div>
      <img class="img-fluid" :src="characters.card_images[0].image_url_small" :alt="characters.name">
    </div>
    <div>
      <h4>{{ characters.name }}</h4>
      <p>{{ characters.type }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  
</style>