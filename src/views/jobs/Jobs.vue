<template>
  <h1>Jobs</h1>
  <div class="job" v-for="job in jobs" :key="job.id">
      <router-link :to="{ name: 'JobDetails', params:{ id: job.id }}">
       <h2>{{ job.title }}</h2>
       </router-link>
  </div>
 
</template>

<script>
export default {
data() {
    return {
        jobs: [
            { id: 1, title: 'Software Developer', deatails: 'loerm' },
            { id: 2, title: 'Web Designer', deatails: 'loerm' },
            { id: 3, title: 'Project Manager ', deatails: 'loerm' }
        ]
    }
},
}
</script>

<style>
.job h2{
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #444;
}
.job h2:hover{
    background: #ddd;
}
.job a {
    text-decoration: none;
}


</style>