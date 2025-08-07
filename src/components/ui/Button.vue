<script setup>
</script>

<template>
  <button class="button">
    <slot />
  </button>
</template>

<style scoped>
  .button {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: var(--spacing-sm);
    border-radius: 15px;
    border: none;
    padding: var(--spacing-sm) var(--spacing-xl);
  }
</style>