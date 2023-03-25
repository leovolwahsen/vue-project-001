<script setup lang="ts">
import axios from 'axios'
import type { IJob } from '../interfaces'

let jobs: IJob[] = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data
// import type { IJob } from '@/interfaces'
// import axios from 'axios'

//const jobs: IJob[] = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data
</script>

<template>
  <div>
    <p>
      There are currently {{ jobs.length }} jobs currently on the german market in the Industry of
      Full-Stack Development.
    </p>
  </div>
  <div>
    <!-- <ul>
      <li>
        Title: {{ jobs[1].title }} Company: <link rel="stylesheet" href={{ jobs[1].url }} />
      </li>
    </ul> -->
    <ul>
      <li v-for="job in jobs">{{ job.title }}</li>
    </ul>
  </div>
  <!-- <p>There are {{ jobs.length }} jobs.</p> -->
</template>
<!-- <a target="_blank" :href="job.url">{{ job.title }}</a>
- {{ job.company }} -->

<style scoped>
li {
  color: #ccc;
  font-size: 1.3rem;
}
a {
  color: rgb(218, 218, 128);
}
</style>
