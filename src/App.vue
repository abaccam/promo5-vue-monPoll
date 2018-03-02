<template>
  <div id="app">
    <img src="./assets/logo.png">
    <CreatePoll/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import CreatePoll from './components/CreatePoll'


export default {
  name: 'App',
  components: {
    CreatePoll
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
