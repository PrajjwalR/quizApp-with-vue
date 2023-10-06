<template>
  <div class="results">
    <p>Your Results...</p>
    <h3>{{ numberOfCorrectAnswers }} / {{ quizQuestionLength }}</h3>
    <RouterLink to="/">Back to home</RouterLink>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import { RouterLink } from "vue-router";

const { numberOfCorrectAnswers, quizQuestionLength } = defineProps([
  "quizQuestionLength",
  "numberOfCorrectAnswers",
]);
</script>

<style scoped>
.results {
  text-align: center;
  padding: 100px 0px;
}
p {
  font-size: 25px;
}
h3 {
  font-size: 80px;
}
</style>
