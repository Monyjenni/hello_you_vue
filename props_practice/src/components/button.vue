<template>
  <div>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">

<button @click="generateName" class="btn btn-primary"> Generate Name!!! </button>

  </div>
</template>

<script>
  export default {
    name: 'ButtonVue',
    props :{
      myName: String
    },
    generateName(){
      const names = ['jessica','jennie','steven','mony']
      const randomName = Math.floor(Math.random() * names.length)
      const newName = names(randomName)
      this.$emit('update:,myName',newName)
      
    }
  }
</script>

<style scoped>

</style>