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
    <h1>------------------------------------------</h1>
    <h2 v-show="ok"> This is V-show !</h2>
    <h1>This is v-for</h1>
    <!-- <li v-for="item in items">
      {{ item.message }}
    </li> -->
    <h2>Inline Handler</h2>
    <v-btn color="green" @click="count ++">Add 1</v-btn>
    <h1>------------------------------------------</h1>
    <p>The total count is :{{ count }}</p>
    <h1>------------------------------------------</h1>
    <eventButton @click="greet">Click me to greet</eventButton>
    <eventButton @click="say('hello')">Say Hello</eventButton>
    <eventButton @click="say('bye')">Say bye</eventButton>
    <h1>------------------------------------------</h1>  
    <v-btn @click="warn('form cant be submitted.', $event)">hi</v-btn>
    <v-btn @click.stop="doSomething">Click Me</v-btn>
    <v-btn @click.prevent="doSomething">Prevent</v-btn>
    <v-btn @click.once="doSomething">Once</v-btn>
    <v-btn @click.self="doSomething">Self</v-btn>
    <h1>------------------------------------------</h1>
    <div @click.capture="handleClick">
      <v-btn>Click me</v-btn>
    </div>
    <h1>------------------------------------------</h1>
    <div @scroll.passive="onScroll">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus suscipit explicabo adipisci, odio voluptas maiores eius ratione enim debitis sapiente provident dignissimos expedita minus sed laborum animi cumque! Excepturi, quis.</p>
    </div>
    <h1>------------------------------------------</h1>
    <ul>
      <li v-for="item in items" v-bind:key="item.id">{{ item }}</li>
    </ul>
    <h1>------------------------------------------</h1>
    <li v-for="anime in animes" v-bind:key="anime.id">
      {{ anime.message }}
    </li>
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
      name : 'Jennie',
      items: ['apple','carrot','peach'],
      animes: [{message:'guts in nutshell'},{message:'I have no enemies!'}]

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
    },
    warn (message,event) {
      if(event) {
        event.preventDefault();
      }
      alert(message)
    },
    doSomething() {
      alert('hey')
    },
    handleClick() {
      console.log("clicked")
    },
    onscroll () {
      console.log('onscroll')
    },

  }
  }
</script>
