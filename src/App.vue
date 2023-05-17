<template>
  <div :style="{ backgroundColor: color, width: '2000px', height: '2000px' }">
    <div id="app">
      <HelloWorld msg="Hello Buddy" />
      <div class="child"></div>
    </div>
    <div id="button">
      <button @click="changeColor">Change backgroundColor</button>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      color: "pink",
    };
  },
  methods: {
    changeColor() {
      //asign randomColor = hashtag to add with random math value and time with 12432343 then we floor
      //floor means here is to asume to take the decimal number
      //toString is to return a string to as a string
      const randomColor =
        "#" + Math.floor(Math.random() * 12432343).toString(16);

      //update the color property with the new color
      //this here is a constructor
      this.color = randomColor;
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
}
#button {
  font-size: 25px;
  border-radius: 15px;
  color: blueviolet;
  padding-bottom: 50px;
  text-align: center;
}
#button button {
  font-size: 30px;
  border-radius: 15px;
}
.child {
  margin-top: 200px;
}
</style>
