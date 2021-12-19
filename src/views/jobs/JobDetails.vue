<template>
  <section class="container">
      <div class="row">
          <div class="col-12">
              <h1>{{job.title}}</h1>
              <p>the job id is {{id}}</p>
              <p>{{job.details}}</p>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    props:['id'],
    data() {
        return {
           job:[]
        }
    },
    mounted() {
        fetch("http://localhost:3000/jobs/" + this.id)
        .then((response)=> response.json())
        .then(data => this.job = data)
        .catch(err => console.log(err.message))
    },
}
</script>

<style>

</style>
