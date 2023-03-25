<script setup lang="ts">
import type { ISkill } from '@/interfaces'
import axios from 'axios'
const skills: ISkill[] = (await axios.get('https://edwardtanguay.vercel.app/share/skills.json'))
  .data
</script>

<template>
  <div class="skills">
    <p>There are {{ skills.length }} skills.</p>
    <ul>
      <li v-for="skill in skills">
        <a target="_blank" :href="skill.url">{{ skill.name }}</a> - {{ skill.description }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
li {
  color: #ccc;
  font-size: 1.3rem;
}
a {
  color: rgb(218, 218, 128);
}
</style>
