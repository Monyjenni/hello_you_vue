<template>
  <div class="hello">
    <h1>Props Practice</h1>
    <p>{{ firstName}} {{ lastName }}</p>
  </div>
</template>

<script>
export default {
  name: 'PropertiesVue',
  // Matching props type is a MUST
  props: {
    firstName : String,
    lastName : String
  }
}
</script>

<style scoped>

</style>
