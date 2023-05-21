<template>
  <div>
  <h2>{{ 2+3+5 }}</h2>
  <h3>{{ 3+6+8}}</h3>
  <!-- inside curly braces__can call the method  -->
  <h2>Add method- {{ add(10,4,5) }}</h2>
  <h2>Multiply method -{{ multiply(num) }}</h2>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    //data properties
    return{
      baseMultiplier : 5,
      //if i pass data properties like (baseValue) no need to use this keyword, not use num
      baseValue:2
    }
  },
  methods:{
    // is like a function
    // a b c are paramter
    add(a,b,c){
      return a + b + c
    },
    //if we use arrow then this dont point to the baseMultiplier
    multiply (num) {
      // baseMultiplier is from return data
      //if no return means nth
      return num * this.baseMultiplier
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
