
<template>
  <div id="app">
    <!-- include greet into this app -->
    <GreetMony name="Jen" heroName="Batman"/>
    <GreetMony name="Jennie" heroName="Superman"/>
    <GreetMony name="Mony" heroName="WonderWoman"/>
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
</template>

<script>
//component lets you beak down your application into small encapsulated parts which can then be composed to make more complex user interface
//component is reusable means we can use diff properties and display diff information
import GreetMony from './components/Greet.vue'
export default {
  name: 'App',
  //specify Greet component
  //Props allows component content to be dynamic

  components: {
    GreetMony,
  } 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
