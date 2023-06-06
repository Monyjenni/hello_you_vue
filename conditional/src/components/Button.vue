<template>
  <div>
    <v-btn v-bind="$attrs" v-on="$listeners" outlined :color="color" @click="awesome = !awesome">
      Button
    </v-btn>
    <h1 v-if="awesome">
      Mony is awesome
    </h1>
    <h2 v-else>Sheesh</h2>
  </div>
</template>

<script>
export default {
  name: 'buttonRendering',
  data() {
    return {
      awesome: false
    }
  },
  props : {
    color : {
    type: String,
    default : "primary" 
    }
  }
}
</script>