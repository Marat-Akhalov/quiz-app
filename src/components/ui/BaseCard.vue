<template>
  <div class="card">
    <slot></slot>
  </div>
</template>

<style scoped>
.card {
  border-radius: 10px;
  border: 2px solid var(--clr-prime);
  overflow: hidden;
}
</style>
