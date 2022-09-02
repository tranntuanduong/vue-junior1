<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="app">
    <Header />
    <RouterView />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  components: {
    Header,
  },
};
</script>

<style scoped>
.app {
  background-color: var(--main-bg);
  overflow: hidden;
}
</style>
