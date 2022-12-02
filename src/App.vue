<!-- SCRIPT -->
<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    name: "App",
    AppHeader,
  }
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