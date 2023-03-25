<script setup lang="ts">
import axios from 'axios'
import type { IJob } from '../interfaces'

let jobs: IJob[] = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data
console.log(jobs)
</script>

<template>
  <div>
    <p>
      There are currently {{ jobs.length }} jobs currently on the german market in the Industry of
      Full-Stack Development.
    </p>
  </div>
  <div>
    <ul>
      <li v-for="job in jobs">
        <a target="_blank" :href="job.url">{{ job.title }}</a> - {{ job.company }}{{ job.title }}
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
