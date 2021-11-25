<template>
  <div class="hello">
    <h2>{{ question.question }}</h2>
    <ol v-show="!isSent">
      <form v-on:submit.prevent="handleSubmit">
        <li
          v-for="(response, index) in question.responses"
          v-bind:key="index"
        >
          <input type="radio" v-bind:id="'input_'+index" v-bind:value="response" v-model="userRes">
          <label v-bind:for="'input_'+index">{{ response.text }}</label>
        </li>
        <button type="submit">Submit</button>
      </form>
    </ol>
    <p v-show="isSent">Answer sent !</p>
  </div>
</template>

<script>
export default {
  name: "Question",
  props: {
    question: Object,
  },
  data() {
    return{
      userRes: null,
      isSent: false,
    }
  },
  methods: {
    handleSubmit() {
      this.isSent= true;
      if(this.userRes.correct) {
        this.$emit("addPoint", 1);
      }
    },
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button {
  color: #21ffe0;
  background-color: black;
  border-color: #21ffe0;
  border-radius: 10px;
}
button:hover {
  box-shadow: 0 0 3px 3px #21ffe0;
}
</style>
