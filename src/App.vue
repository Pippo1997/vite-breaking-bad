<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import CharactersList from './components/CharactersList.vue';
export default {
  components:{
    AppHeader,
    CharactersList
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
  @use './styles/generals.scss' as *;
</style>
