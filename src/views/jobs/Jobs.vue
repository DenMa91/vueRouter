<template>
  <section class="container">
      <div class="row">
              <h1 class="text-center">Jobs</h1>
                  <div class="card col-4" v-for="job in jobs" :key="job.id">
                    <div class="card-body">
                        <h5 class="card-title">{{job.title}}</h5>
                        <h6 class="card-subtitle mb-2 text-muted">{{job.id}}</h6>
                        <p class="card-text">job.details</p>
                        <a href="#" class="card-link">scopri di piu</a>
                    </div>
                  </div>          
          </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            jobs: [
                {title: 'UX Designer', id:1, details:'lorem 1'},
                {title: 'WEB Developer', id:2, details:'lorem 2'},
                {title: 'VUE Developer', id:3, details:'lorem 3'}
            ]
        }
    },
}
</script>

<style>

</style>