<template>
  <div class="box">
    <h3>{{triviaQuestion.question}}</h3>
    <div class="answers-div">
      <h4>Lists of Answers</h4>
      <div class="answers">
        <p>answer 1</p>
        <p>answer 2</p>
        <p>answer 3</p>
        <p>answer 4</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "QuestionBox",
  props: {
    triviaQuestion: Object
  }
};
</script>

<style>
.answers p {
  border: 1px solid;
  margin-bottom: 3px;
  border-collapse: separate;
  cursor: pointer;
}

.answers p:hover {
  background: rgb(238, 238, 238);
}

.box {
  padding: 40px;
}

h3 {
  border-bottom: 2px solid;
  padding-bottom: 10px;
}
.answers-div {
  margin-top: 10px;
}
</style>