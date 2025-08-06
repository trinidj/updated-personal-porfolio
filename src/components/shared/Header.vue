<script setup>
  import Button from '@/components/ui/Button.vue';
  import { Mail } from 'lucide-vue-next';
</script>

<template>
  <header id="header-section">
    <nav>
      <div class="site-title-container">
        <span class="site-title">John Trinidad</span>
      </div>

      <div class="navigation-container">
        <ul class="list">
          <li class="list-item">Project</li>
          <li class="list-item">About</li>
          <li class="list-item">Experience</li>
          <li class="list-item">Skills</li>
        </ul>
      </div>

      <div class="socials-container">
        <Button>
          <Mail />
          <span>Contact Me</span>
        </Button>
      </div>
    </nav>
  </header>
</template>

<style scoped>
  nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
</style>