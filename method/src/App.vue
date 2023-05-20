<template>
  <div>
  <h2>{{ 2+3+5 }}</h2>
  <h3>{{ 3+6+8}}</h3>
  <!-- inside curly braces__can call the method  -->
  <h2>Add method- {{ add() }}</h2>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return{

    }
  },
  methods:{
    // is like a function
    add(){
      return 2+3+3+5
    }
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
