<script>
import AppHeader from './components/AppHeader.vue';
import CharactersList from './components/CharactersList.vue';
import AppMainVue from './components/AppMain.vue';

import { store } from './store.js'
import axios from 'axios';

export default {
  components:{
    AppHeader,
    CharactersList,
    AppMainVue,
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
        store.CharactersList = response.data.data.slice(0, 25);
      })
    }
  }
}
</script>

<template lang="">
  <div>
    <AppHeader/>
    <AppMain />
    <CharactersList/>
  </div>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
</style>
