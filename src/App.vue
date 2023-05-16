<template>
  <div id="app">
    <HelloWorld msg="Hello Buddy" />
    <div id="button">
      <button v-on:click="counter += 1">Change Color</button>

      <p>The button has been clicked {{ counter }} times</p>
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
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#button {
  font-size: 20px;
  border-radius: 15px;
  color: blueviolet;
  padding-bottom: 50px;
}
#button button {
  font-size: 30px;
  border-radius: 15px;
}
</style>
