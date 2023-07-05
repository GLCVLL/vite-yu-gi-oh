<script>
import axios from 'axios';
import { apiUri } from './data';
import AppMain from './components/AppMain.vue';
import SearchForm from './components/searchForm.vue';
import { store } from './data/store.js';
export default {
  components: { AppMain, SearchForm },
  data() {
    return {
      typeFilter: '',
    }
  },
  methods: {
    fetchCharacters(endpoint = apiUri) {
      axios.get(endpoint).then(res => {
        store.characters = res.data.docs;
      })
    },
    searchTypes() {
      const endpoint = `${endpoint}?eq${this.typeFilter}`;
    }
  },
  created() {
    this.fetchCharacters();
  },
};
</script>
<template>
  <header>
    <SearchForm @change="searchTypes" />
  </header>
  <AppMain />
  <footer></footer>
</template>
<style lang="scss">
@use './assets/scss//style.scss';
</style>