<script setup>
import { RouterLink } from "vue-router"

const routes = [
  {
    name: "Home",
    path: "/",
  },
  {
    name: "About",
    path: "/about",
  },
]
</script>

<template>
  <header>
    <RouterLink to="/" class="logo">
      <img src="../assets/logo.svg" alt="" />
      <span>Vue App</span>
    </RouterLink>

    <nav>
      <ul>
        <li v-for="route in routes" :key="route.path">
          <RouterLink :to="route.path">{{ route.name }}</RouterLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 0.0625rem solid #ffffff20;
  padding: 1rem 0;
  margin-bottom: 1rem;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  text-decoration: none;
  color: #fff;

  img {
    width: 1.5rem;
  }

  span {
    font-weight: 600;
  }
}

nav ul {
  display: flex;

  li {
    list-style: none;
    a {
      text-decoration: none;
      color: #fff;
      border-radius: 0.5rem;
      transition: 0.1s;
      padding: 0.5rem 0.75rem;
      &:hover {
        background: #ffffff20;
      }
    }
  }
}
</style>
