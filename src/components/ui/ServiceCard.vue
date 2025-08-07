<script setup>

</script>

<template>
  <div class="service-card">
    <div class="icon-container">
      <slot />
    </div>

    <div class="service-content">
      <div class="service-header">
        <slot />
      </div>

      <div class="service-description">
        <slot />
      </div>
    </div>
  </div>
</template>

<style scoped>
  
</style>