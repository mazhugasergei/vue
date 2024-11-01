<script setup lang="ts">
import { RouterView } from "vue-router"
import Header from "./components/Header.vue"
</script>

<template>
  <div class="wrapper">
    <Header />
    <RouterView />
  </div>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  background: #5d8974;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans",
    "Helvetica Neue", sans-serif;
  font-size: 0.875rem;
  color: #fff;
}

.wrapper {
  max-width: 30rem;
  margin: 0 auto;
}
</style>
