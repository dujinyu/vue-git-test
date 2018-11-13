<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <HelloWorld/> -->
    <test />
    <world />
    <hello />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Test from './components/test'
import World from './components/world'
import Hello from './components/hello'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Test,
    World,
    Hello
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
