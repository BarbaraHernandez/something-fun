<template>
  <div id="app">
    <HelloWorld msg=" you are my favorite"/>
  <!-- Game components below -->
    <Gem imageSource="1"></Gem>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Gem from './components/Gem'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Gem
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
