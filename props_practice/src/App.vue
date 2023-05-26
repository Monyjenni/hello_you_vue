<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <PropertiesVue :firstName="'Chansovanmony'" :lastName="'Yoeun'"/>
  </div>
</template>

<script>

import PropertiesVue from './components/props.vue'

export default {
  name: 'App',
  components: {
    PropertiesVue
  }
}
</script>

<style>

#app {
 text-align: center;
}
body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}
</style>
