<script>
export default {
  props:{
    characters: Object
  }
}
</script>

<template lang="">
  <div class="col-12 col-md-3 mt-3">
    <div class="cards-card">
      <div class="card-image">
        <img class="img-fluid" :src="characters.card_images[0].image_url" :alt="characters.name">
      </div>
      <div class="card-info">
        <h4>{{ characters.name }}</h4>
        <p>{{ characters.type }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .cards-card{
    background-color: rgba(212,143,56,255);
    text-align: center;
    height: 100%;
    width: 100%;

      h4{
        text-transform: uppercase;
        color: white ;

        .card-info{
          padding: 10px;
        }
      }
  }
</style>