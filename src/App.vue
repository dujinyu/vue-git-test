<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <test />
    <hello />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Test from './components/test'
import Hello from './components/hello'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Test,
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
