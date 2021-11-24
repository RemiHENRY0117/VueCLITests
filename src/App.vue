<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Quiz msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Quiz from './components/Quiz.vue'

export default {
  name: 'App',
  components: {
    Quiz
  }
}
</script>

<style>
html { background-color: black;}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  color: white;
}
</style>
