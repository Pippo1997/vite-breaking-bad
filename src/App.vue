<script>
import AppHeader from './components/AppHeader.vue';
import CharactersList from './components/CharactersList.vue';
import AppFilter from './components/AppFilter.vue';

import { store } from './store.js'
import axios from 'axios';

export default {
  components:{
    AppHeader,
    CharactersList,
    AppFilter,
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
      let MyUrl = `${store.url}${store.selectedGenere}`;

      axios.get(MyUrl).then((response) => {
        store.CharactersList = response.data.data;
      })
    }
  }
}
</script>

<template lang="">
  <div>
    <AppHeader />
    <AppFilter @filter="getCharacters"/>
    <CharactersList />
  </div>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
</style>
