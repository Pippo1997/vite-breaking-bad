<script>
import CharactersCard from './CharactersCard.vue';
import { store } from '../store.js'

export default {
  components:{
    CharactersCard
  },
  data(){
    return{
        store
    }
  }
}
</script>
<template lang="">
  <div class="container mt-5">
    <div class="row">
      <div class="col-12">
        <CharactersCard v-for="(item, index) in store.CharactersList" :key="index" :characters="item" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  
</style>