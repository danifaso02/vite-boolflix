<script>
import { store } from "./store";

export default {
  name: "AppHeader",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div>
    <input type="text" v-model="store.textToSearch" placeholder="Cerca pure">
    <button @click="$emit('performSearch')">Invio</button>
  </div>
</template>

<style scoped></style>


