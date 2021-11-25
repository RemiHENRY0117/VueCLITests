<template>
  <div id="app">
    <img class="logo" alt="Vue logo" src="./assets/bflogo.png">
    <Quiz 
      v-for="question in quizcontent"
      v-bind:quizcontent="question"
      v-bind:key="question.id"
    />
  </div>
</template>

<script>
import Quiz from './components/Quiz.vue'

export default {
  name: 'App',
  components: {
    Quiz
  },
  data () {
    return {
      quizcontent: [
        {
          question: "Which is the first Battlefield game ?",
          responses: [
              { text: "Battlefield 1" },
              { text: "Battlefield 2042"},
              { text: "Battlefield 1942", correct: true },
              { text: "None of the above" }
          ]
        },
        {
          question: "Which is the main Battlefield studio ?",
          responses: [
              { text: "DICE", correct: true },
              { text: "EA" },
              { text: "Valve" },
              { text: "None of the above" }
          ]
        },
        {
          question: "Which year is Battlefield 2042 taking place ?",
          responses: [
              { text: "2021" },
              { text: "2041" },
              { text: "2043" },
              { text: "None of the above", correct: true }
          ]
        },
        {
          question: "In which state did Battlefield 2042 came out ?",
          responses: [
              { text: "Pre-Alpha", correct: true },
              { text: "Alpha" },
              { text: "Beta" },
              { text: "1.0" }
          ]
        },
        {
          question: "Which weapon needs balancing in Battlefield 2042 right now ?",
          responses: [
              { text: "Absolutely none, everything is perfectly fine" },
              { text: "Absolutely none, everything is perfectly fine" },
              { text: "Absolutely none, everything is perfectly fine" },
              { text: "None of the above (duh !)", correct: true }
          ]
        },
        {
          question: "When did Battlefield 2042 standard edition came out ?",
          responses: [
              { text: "2021-11-12" },
              { text: "2021-10-20" },
              { text: "2021-11-19", correct: true },
              { text: "None of the above" }
          ]
        },
        {
          question: "Quel est le muscle ?",
          responses: [
              { text: "Kamoulox", correct: true },
              { text: "Oui" },
              { text: "Je savais mais je sais plus, tu vois ?" },
              { text: "None of the above" }
          ]
        }
      ]
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
