<!-- SCRIPT -->
<script>
import AppHeader from './components/AppHeader.vue';
import { store } from './components/store';
import axios from "axios";
import AppMain from './components/AppMain.vue';
import AppCard from './components/AppCard.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppCard,
  },
  data() {
    return {
      store,
    };
  },
  methods: {
    getResults() {
      axios
      .get("https://api.themoviedb.org/3/movie/", {
        params: {
          api_key:"28f09a904a6b5c94bd677ec078cb8a67",
          query: store.textToSearch,
          lenguage:"it-IT",
        },
      })
      .then((response) => {
        this.store.movies = response.data.results;
      });
    },
  },
};
</script>

<!-- TEMPLATE -->
<template>
  <div>
    <AppHeader @performSearch="getResults" />
    <AppMain />
  </div>
</template>

<!-- STYLE -->
<style scoped>
</style>