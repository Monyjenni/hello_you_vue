<template>
  <div>
    <v-btn v-on="$listeners" v-bind="$attrs" :color="color">Click Me</v-btn>
  </div>
</template>

<script>
  export default {
    name: 'eventButton',
    props : {
      color : {
        type : String
      }
    }
  }
</script>
