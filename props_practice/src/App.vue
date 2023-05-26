<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <PropertiesVue :firstName= 'firstName' :lastName= 'lastName'/>
  </div>
</template>

<script>

import PropertiesVue from './components/props.vue'

export default {
  name: 'App',
  data(){
    return {
      firstName: 'Yoo',
      lastName: 'Im Sensei'
    }
 
  },
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
