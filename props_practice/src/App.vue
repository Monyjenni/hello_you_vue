<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <PropertiesVue :description= 'description' />
    <ButtonVue />
    <p> {{ newName }}</p>
  </div>
</template>

<script>

import PropertiesVue from './components/props.vue'
import ButtonVue from './components/button.vue'

export default {
  name: 'App',
  data(){
    return {
     description: "let's generate new name!",
     newName: 'Casca'
    }
 
  },
  components: {
    PropertiesVue,
    ButtonVue
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
