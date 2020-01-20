<template>
  <div id="app">
    <HelloWorld msg=" you are my favorite" />
    <!-- Game components below -->
    <Gem :imageSource="imageSource"></Gem>
    <input type="number" v-model="imageSource" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Gem from "./components/Gem";

export default {
  name: "app",
  data() {
    return {
      imageSource: 1
    };
  },

  components: {
    HelloWorld,
    Gem
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
