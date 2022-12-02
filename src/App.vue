<!-- SCRIPT -->
<script>
import AppHeader from './components/AppHeader.vue';
import { store } from './components/store';

export default {
  name: "App",
  components: {
    AppHeader,
  },
  data() {
    return {
      store,
    };
  },
  methods: {
    getResults() {
      axios.get("https://api.themoviedb.org/3/movie/550?api_key=28f09a904a6b5c94bd677ec078cb8a67", {
        params: {
          api_key:'28f09a904a6b5c94bd677ec078cb8a67',
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
  </div>
</template>

<!-- STYLE -->
<style scoped>
</style>