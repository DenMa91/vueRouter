<template>
  <section class="container">
      <div class="row">
          <div class="col-12">
              <h1>Job Details</h1>
              <p>the job id is {{id}}</p>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    props:['id'],
    data() {
        return {
           
        }
    },
}
</script>

<style>

</style>
