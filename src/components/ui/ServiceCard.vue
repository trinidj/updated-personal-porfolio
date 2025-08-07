<script setup>
  const props = defineProps({
    title: {
      type: String,
      default: '',
    },
    desc: {
      type: String,
      default: '',
    },
  });
</script>

<template>
  <div class="service-card">
    <div class="icon-container">
      <slot />
    </div>

    <div class="content-container">
      <div class="service-content">
        <div class="service-header">
          {{ props.title }}
        </div>

        <div class="service-description">
          {{ props.desc }}
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .service-card {
    display: flex;
    flex-direction: row;
    padding: var(--spacing-xl);
    background: hsl(from var(--color-background-primary) h s calc(l - 3) / 0.5);
  }
</style>