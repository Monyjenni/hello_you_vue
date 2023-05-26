<template>
  <div class="hello">
    <h1>Props Practice</h1>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: 'PropertiesVue',
  // Matching props type is a MUST
  props: {
    description: String
  }
}
</script>

<style scoped>

</style>
