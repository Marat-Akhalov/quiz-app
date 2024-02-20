<script setup>
import { ref } from 'vue'
import q from '@/data/data.json'

const quizes = ref(q)
</script>

<template>
  <h2>Quiz App</h2>
</template>

<style>
@import '@/assets/main.css';
</style>
