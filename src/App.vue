<script setup>
import { ref } from 'vue'
import q from '@/data/data.json'

import QuizList from '@/components/QuizList.vue';

const quizes = ref(q)
</script>

<template>
  <QuizList :quizes="quizes" />
</template>

<style>
@import '@/assets/main.css';
</style>
