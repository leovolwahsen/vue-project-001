<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <Suspense>
    <div>
      <h1>The Info Site</h1>
      <nav>
        <RouterLink to="/">Welcome</RouterLink>
        <RouterLink to="/jobs">Jobs</RouterLink>
        <RouterLink to="/skills">Skills</RouterLink>
      </nav>
      <RouterView />
    </div>
  </Suspense>
</template>

<style scoped lang="scss">
nav {
  display: flex;
  gap: 0.5rem;
  background-color: #222;
  padding: 0.5rem 1rem;
  a {
    color: #ccc;
    text-decoration: none;
    font-size: 1.3rem;
  }
}
h1 {
  color: orange;
}
a.router-link-active {
  color: orange;
}
</style>
