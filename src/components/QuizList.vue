<script setup>
import { toRefs, defineProps } from "vue"

import QuizListItem from "./QuizListItem.vue";

const props = defineProps({
  quizes: {
    type: Array,
    required: true,
  }
})

const { quizes } = toRefs(props)
</script>

<template>
  <ul class="list list-reset">
    <QuizListItem
      v-for="quiz in quizes"
      :key="quiz.id"
      :name="quiz.name"
      :img-path="quiz.img"
      :questions="quiz.questions" />
  </ul>
</template>

<style scoped>
.list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
</style>
