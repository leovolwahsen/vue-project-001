<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <h1>The Info Site</h1>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>
  <RouterView />
</template>

<style scoped>
nav {
  display: flex;
  gap: 0.5rem;
  background-color: #222;
  padding: 0.5rem 1rem;
}
h1 {
  color: orange;
}
a {
  color: #ccc;
  text-decoration: none;
  font-size: 1.3rem;
}
a.router-link-active {
  color: orange;
}
</style>
