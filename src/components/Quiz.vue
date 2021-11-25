<template>
  <div id="quiz">
      <Question
        v-for="(question, index) in quizData"
        v-bind:key="index"
        v-bind:question="question"
        v-on:addPoint="handleAddPoint"
        />
    <h2>You've got {{points}} points !</h2>
  </div>

</template>

<script>
import Question from './Question.vue'


export default {
    name: 'Quiz',
    components: {
        Question
    },
    props: {
        quizData: Array,
    },
    data() {
        return{
            points: 0,
        }
    },
    methods: {
        handleAddPoint (points) {
            this.points=this.points+points
        }
    },
}
</script>

<style>

</style>
