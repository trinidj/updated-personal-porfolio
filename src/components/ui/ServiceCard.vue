<script setup>
  const props = defineProps({
    title: {
      type: String,
      default: '',
    },
    description: {
      type: String,
      default: '',
    },
    icon: {
      type: Object,
      default: null,
    },
  });
</script>

<template>
  <div class="service-card">
    <div class="icon-container">
      <div class="icon">
        <component 
          v-if="props.icon" 
          :is="props.icon" 
        />
        <slot v-else />
      </div>
    </div>

    <div class="content-container">
      <div class="service-content">
        <div class="service-header">
          <h4>{{ props.title }}</h4>
        </div>

        <div class="service-description">
          <p>{{ props.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .service-card {
    display: flex;
    flex-direction: row;
    /* align-items: center; */
    gap: var(--spacing-base);
    padding: var(--spacing-lg);
    background: hsl(from var(--color-background-primary) h s calc(l - 3) / 0.5);
    border: 1px solid hsl(from var(--color-accent-primary) h s calc(l - 10) / 0.5);
    border-radius: 15px;
  }

  .icon {
    display: flex;
    color: #99E1D9;
    border-radius: 10px;
    background: hsl(from var(--color-accent-secondary) h s l / 0.5);
    padding: var(--spacing-sm);
  }

  .service-content {
    display: flex;
    flex-direction: column;
    gap: var(--spacing-sm);
  }

  .service-header h4 {
    font-size: var(--text-xl);
  }

  .service-description p {
    color: hsl(from var(--color-text-primary) h s l / 0.7);
  }
</style>