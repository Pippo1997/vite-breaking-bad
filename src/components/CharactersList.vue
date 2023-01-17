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
  <main class="container mt-5 bg-white">
    <div class="row">
      <div class="col-12 bg-black text-light p-3">
        Carte trovate
      </div>
    </div>
    <div class="row">
        <CharactersCard v-for="(item, index) in store.CharactersList" :key="index" :characters="item" />
    </div>
  </main>
</template>

<style lang="scss">
  
</style>