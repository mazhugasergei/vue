<script setup>
import { ref } from "vue"
import Card from "../components/Card.vue"

const count = ref(0)
</script>

<template>
  <Card class="card">
    <h1>Count: {{ count }}</h1>
    <button @click="count--">-</button>
    <button @click="count++">+</button>
  </Card>
</template>

<style scoped lang="scss">
.card {
  display: flex;
  align-items: center;
}

h1 {
  font-size: 2rem;
  margin-right: auto;
}

button {
  cursor: pointer;
  width: 3rem;
  height: 3rem;
  background: #658d7a;
  font-size: 1rem;
  color: #fff;
  border-radius: 100vmax;
  border: 0;
  transition: 0.1s;

  &:hover {
    background: #fff;
    color: #658d7a;
  }
}
</style>
