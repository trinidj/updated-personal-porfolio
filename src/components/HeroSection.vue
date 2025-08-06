<script setup>
  import Button from '@/components/ui/Button.vue';
  import { ArrowRight } from 'lucide-vue-next';
</script>

<template>
  <section id="hero-section">
    <div class="hero-container">
      <div class="title">
        <span>John Trinidad</span>
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
    height: 500px;
    width: 500px;
    background-image: 
      radial-gradient(circle at 45% 40%, rgba(59, 130, 246, 0.3), transparent 40%),
      radial-gradient(circle at 55% 60%, rgba(59, 130, 246, 0.25), transparent 35%),
      radial-gradient(closest-side, rgba(255, 230, 0, 0.21), #1A1A1A);
    background-position: center center;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    margin: 0 auto;
  }
</style>