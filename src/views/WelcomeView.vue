<script setup lang="ts">
import { ref } from 'vue'
const showButton = ref(true)
const greeting = 'Welcome to this site'
const message = ref('This site contains information about available jobs.')

const changeMessage = () => {
  message.value = 'This site also contains skills you need for IT jobs.'
  showButton.value = false
}
</script>

<template>
  <div class="welcome">
    <h2>{{ greeting }}</h2>
    <p>{{ message }}</p>

    <button v-if="showButton" @click="changeMessage">more info</button>
  </div>
</template>

<style scoped>
h2 {
  color: olive;
}

p {
  color: #aaa;
  font-style: italic;
}
</style>
