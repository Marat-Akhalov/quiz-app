<script setup>
import { toRefs } from "vue"

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

  </ul>
</template>
