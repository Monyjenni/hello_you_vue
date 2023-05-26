<template>
  <div>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">

<button @click="generateName" class="btn btn-primary"> Generate UwU!!! </button>

  </div>
</template>

<script>
  export default {
    name: 'ButtonVue',
    props :{
      newName: String
    },
  }
</script>

<style scoped>

</style>