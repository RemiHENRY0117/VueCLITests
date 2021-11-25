<template>
  <div id="app">
    <img class="logo" alt="Vue logo" src="./assets/bflogo.png">
    <Quiz
      v-bind:quizData="quizData"
    />
  </div>
</template>

<script>
import Quiz from './components/Quiz.vue';
import QuizData from './data.js';

export default {
  name: 'App',
  components: {
    Quiz
  },
  data () {
    return {
      quizData: QuizData
    }
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
.logo {
  width: 60%;
}
</style>
