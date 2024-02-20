<script setup>
const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  imgPath: {
    type: String,
    required: true,
  },
  questions: {
    type: Array,
    required: true,
  }
})

const { name, imgPath, questions } = props
</script>

<template>
  <base-card>
    <li class="list__item">
      <img
        class="list__img"
        :src="imgPath"
        alt="Discipline illustration">
      <div class="list__text-wrap">
        <h2 class="list__title">{{ name }}</h2>
        <p class="list__questions-amount">{{ questions.length }} questions</p>
      </div>
    </li>
  </base-card>
</template>
