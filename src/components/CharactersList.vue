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
    <div class="d-flex justify-content-between flex-wrap">
        <CharactersCard v-for="(item, index) in store.CharactersList" :key="index" :characters="item" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
  
</style>