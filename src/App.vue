<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import CharactersList from './components/CharactersList.vue';

import { store } from './store.js'

export default {
  components:{
    AppHeader,
    CharactersList,
  },
  data(){
    return{
      store
    }
  },
  created(){
    this.getCharacters();
  },
  methods:{
    getCharacters(){
      axios.get(store.url).then((response) => {
        store.CharactersList = response.data.data
      })
    }
  }
}
</script>

<template lang="">
  <div>
    <AppHeader/>
    <CharactersList/>
  </div>
</template>

<style lang="scss" scoped>
  @use './styles/general.scss' as *;
</style>
