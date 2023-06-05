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
    <eventButton @click="greet">Click me to greet</eventButton>
    <eventButton @click="say('hello')">Say Hello</eventButton>
    <eventButton @click="say('bye')">Say bye</eventButton>
    
    <!-- <h1>Passing Custom Argument to Event Handler Method ! </h1>
    <p v-if="msg"> {{ msg}} </p> -->
  </div>
</template>
<script>
  import buttonRendering from '../components/Button'
  import eventButton from '../components/EvenButton'
  export default {
    name: 'HomePage',
    components: {
      buttonRendering,
      eventButton
    },
    data() {
    return {
      ok : true,
      // items : [{message : 'Foo'},{message: 'Bar'} ]
      count:0,
      name : 'Jennie'
    }
  },
  methods : {
    greet() {
      alert(`Hello ${this.name}`)
      console.log("it's working ",name)
    },
    say(message) {
      //message is a parameter that represents the string passed to the say method when it is called.
      alert(message)
    }
  }
  }
</script>
