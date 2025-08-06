<script setup>
  import Button from '@/components/ui/Button.vue';
  import { ArrowRight } from 'lucide-vue-next';
</script>

<template>
  <section id="hero-section">
    <div class="hero-container">
      <div class="title">
        <a>John Trinidad</a>
      </div>

      <div class="subtitle">
        <span></span>
      </div>

      <div class="call-to-action">
        <Button>
          <span>View Project</span>
          <ArrowRight />
        </Button>

        <Button>
          <span>Contact Me</span>
        </Button>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .hero-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 1000px;
    width: 1000px;
    background-image: 
      radial-gradient(closest-side, rgba(255, 200, 0, 0.2), var(--color-background-primary)),
      radial-gradient(closest-side, rgba(0, 213, 255, 0.6), var(--color-background-primary));
    background-position: center center;
    position: relative;
    margin: 0 auto;
  }
</style>