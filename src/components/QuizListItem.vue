<script setup>
import { defineProps, toRefs } from 'vue';

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

const { name, imgPath, questions } = toRefs(props)
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

<style scoped>
.list__item {
  max-width: 300px;
  cursor: pointer;
}

.list__img {
  width: 100%;
  min-height: 190px;
  object-fit: cover;
}

.list__text-wrap {
  padding: 20px;
}
</style>
