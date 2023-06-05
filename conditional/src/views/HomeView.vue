<template>
  <div >
    <buttonRendering color="primary"/>
    <div v-if="type === 'A' ">
      A
    </div>
    <div v-else-if="type==='B' " >
      B
    </div>
    <div v-else-if="type==='C' " >
      C
    </div>
    <div v-else-if="type==='D' " >
      D
    </div>
    <div v-else>
      Not A/B/C
    </div>
    <h2 v-show="ok"> This is V-show !</h2>
    <h1>This is v-for</h1>
    <!-- <li v-for="item in items">
      {{ item.message }}
    </li> -->
    <h2>Inline Handler</h2>
    <v-btn color="green" @click="count ++">Add 1</v-btn>
    <p>The total count is :{{ count }}</p>
    <v-btn @click="greet">Click me to greet</v-btn>
  </div>
</template>
<script>
  import buttonRendering from '../components/Button'
  export default {
    name: 'HomePage',
    components: {
      buttonRendering
    },
    data() {
    return {
      ok : true,
      // items : [{message : 'Foo'},{message: 'Bar'} ]
      count:0,
      name : 'Jenn'
    }
  },
  method : {
    greet() {
      alert(`Hello ${this.name}`)
    }
  
  }
  }
</script>
