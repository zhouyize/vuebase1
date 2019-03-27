<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Music/>
    <!--
    <Parent/>
    -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Parent from './components/Parent'
import Music from './components/Music'


export default {
  name: 'App',
  components: {
    HelloWorld,
    Parent,
    Music
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
