<script setup>
  import Button from '@/components/ui/Button.vue';
  import { Mail } from 'lucide-vue-next';
  import { animate } from 'animejs';

  const navItems = ['Projects', 'About', 'Experience', 'Skills'];

  const slideIn = (event) => {
    animate(event.target, {});
  };

  const slideOut = (event) => {
    animate(event.target, {});
  }
</script>

<template>
  <header id="header-section">
    <nav>
      <div class="site-title-container">
        <span class="site-title">John Trinidad</span>
      </div>

      <div class="navigation-container">
        <ul class="list">
          <li 
            v-for="item in navItems" 
            :key="item" 
            class="list-item" 
            @mouseover="slideIn" 
            @mouseout="slideOut"
          >
            <a href="">{{ item }}</a>
          </li>
        </ul>
      </div>

      <div class="socials-container">
        <Button class="contact-button">
          <Mail 
            :size="16"
          />
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
    background: hsl(from var(--color-background-primary) h s calc(l - 5) / 0.1);
    padding: var(--spacing-lg) var(--spacing-5xl);
    border-bottom: 1px solid hsl(from var(--color-background-primary) h s calc(l + 10));
  }

  .site-title {
    font-size: var(--text-2xl);
    font-weight: 700;

    background-image: linear-gradient(to right, #99E1D9, #F0F7F4);

    background-clip: text;
    -webkit-background-clip: text; 

    color: transparent;
    -webkit-text-fill-color: transparent; 
  }

  .list {
    display: flex;
    flex-direction: row;
    list-style-type: none;
    gap: var(--spacing-xl);
    cursor: pointer;
    position: relative;
  }

  .contact-button {
    background: hsl(from var(--color-background-primary) h s calc(l - 10) / 0.2);
    border: 1px solid hsl(from var(--color-background-primary) h s calc(l + 10));
    color: white;
    transition: all 0.2s ease;
  }

  .contact-button:hover {
    cursor: pointer;
    background-color: hsl(from var(--color-accent-primary) h s l / 0.2);
    border: 1px solid var(--color-accent-secondary);
  }

  .list-item {
    position: relative;
    font-weight: 500;
    color: hsl(from var(--color-text-primary) h s calc(l + 5) / 0.5);
  }
  
  .list-item a {
    text-decoration: none;
  }

  .list-item a:link, a:visited {
    color: hsl(from var(--color-text-primary) h s calc(l + 5) / 0.5);
  }
  
  .list-item a:hover {
    color: var(--color-accent-primary);
  }

  .list-item::after {
    content: '';
    position: absolute;
    left: 0;
    width: 0; 
    height: 2px; 
    transition: width 0.3s ease; 
    background-color: var(--color-accent-primary);
    bottom: -5px;
  }

  .list-item:hover::after {
    width: 100%; 
  }

  @media (max-width: 768px) {
    nav {
      padding: var(--spacing-base) var(--spacing-xl);
    }

    .site-title {
      font-size: var(--text-xl);
    }

    .list {
      gap: var(--spacing-base);
    }

    .contact-button {
      padding: var(--spacing-sm) var(--spacing-base);
    }

    .contact-button span {
      display: none;
    }
  }

  @media (max-width: 480px) {
    nav {
      padding: var(--spacing-base) var(--spacing-lg);
    }

    .site-title {
      font-size: var(--text-lg);
    }

    .navigation-container {
      display: none;
    }

    .contact-button {
      padding: var(--spacing-xs) var(--spacing-sm);
    }
  }
</style>