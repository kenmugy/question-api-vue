<template>
  <div id="app">
    <Header />
    <QuestionBox :triviaQuestion="questions[id]" />
  </div>
</template>

<script>
import Header from "./components/Header";
import QuestionBox from "./components/QuestionBox";

export default {
  name: "App",
  components: {
    Header,
    QuestionBox
  },
  data() {
    return {
      questions: [],
      id: 0
    };
  },
  created() {
    const api =
      "https://opentdb.com/api.php?amount=10&category=27&type=multiple";
    fetch(api, { method: "GET" })
      .then(res => res.json())
      .then(data => (this.questions = data.results))
      .catch(err => console.log(err));
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
