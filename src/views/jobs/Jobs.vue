<template>
  <section class="container">
      <div class="row">
              <h1 class="text-center">Jobs</h1>
                <div class="p-3 col-4 cardContainer"  v-for="job in jobs" :key="job.id">
                  <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">{{job.title}}</h5>
                        <h6 class="card-subtitle mb-2 text-muted">{{job.id}}</h6>
                        <p class="card-text">job.details</p>
                        <router-link :to="{name:'JobDetails', params:{id: job.id}}" class="card-link">scopri di piu</router-link>
                    </div>
                  </div>
                </div>          
          </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            jobs: []
        }
    },
    mounted() {
        fetch("http://localhost:3000/jobs")
        .then((response)=> response.json())
        .then(data => this.jobs = data)
        .catch(err => console.log(err.message))
    },
}
</script>

<style>

</style>