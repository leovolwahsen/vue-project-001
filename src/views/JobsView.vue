<script setup lang="ts">
import axios from 'axios'

const jobs: IJob[] = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data
</script>
<template>
  <div>
    <p>This is the jobs page.</p>
    <p>There are {{ jobs.length }} jobs.</p>

    <ul>
      <li v-for="job in jobs">
        {{ job.title }} at <br />
        <b>{{ job.company }}</b>
      </li>
    </ul>
  </div>
</template>
<a target="_blank" :href="job.url">{{ job.title }}</a>
- {{ job.company }}

<style scoped>
li {
  color: #ccc;
  font-size: 1.3rem;
}
a {
  color: rgb(218, 218, 128);
}
</style>
