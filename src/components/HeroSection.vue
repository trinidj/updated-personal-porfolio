<script setup>
  import Button from '@/components/ui/Button.vue';
  import { ArrowRight } from 'lucide-vue-next';  
</script>

<template>
  <section id="hero-section">
    <div class="hero-container">
      <div class="title">
        <h1>
          <span class="first-name">John</span>
          <span class="last-name">Trinidad</span>
        </h1>
      </div>

      <div class="subtitle">
        <p>Front-End Developer. Crafting beautiful, responsive user interfaces with modern web technologies and clean, efficient code.</p>
      </div>

      <div class="call-to-action">
        <Button class="view-projects">
          <span>View Projects</span>
          <ArrowRight 
            :size="16"
          />
        </Button>

        <Button class="contact-me">
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
    gap: var(--spacing-xl);
    height: 800px;

    background-image: 
      radial-gradient(closest-side, 
        rgba(0, 213, 255, 0.4) 0%, 
        rgba(0, 213, 255, 0.3) 30%, 
        rgba(0, 213, 255, 0.15) 60%, 
        rgba(0, 213, 255, 0.05) 80%, 
        transparent 100%
      ),
      radial-gradient(closest-side, 
        rgba(4, 255, 209, 0.4) 0%, 
        rgba(4, 255, 209, 0.3) 30%, 
        rgba(4, 255, 209, 0.15) 60%, 
        rgba(4, 255, 209, 0.05) 80%, 
        transparent 100%
      );
    background-position: 
      30% 50%,    
      70% 50%;   
    background-size:
      700px 700px,  
      700px 700px;  
    background-repeat: no-repeat;
    margin: 0 auto;
  }

  .title {
    font-size: var(--text-5xl);
  }

  .title h1 {
    display: flex;
    gap: var(--spacing-base);
  }

  .first-name {
    color: white;
  }

  .last-name {
    background-image: linear-gradient(to right, #00eeff, #00949e);

    background-clip: text;
    -webkit-background-clip: text; 

    color: transparent;
    -webkit-text-fill-color: transparent; 
  }

  .subtitle {
    font-size: var(--text-3xl);
    text-align: center;
    font-weight: 600;
    color: hsl(from #ffffff h s calc(l - 5) / 0.6);
    width: 50%;
  }

  .call-to-action {
    display: flex;
    flex-direction: row;
    gap: var(--spacing-xl);
  }

  .view-projects {
    background: linear-gradient(
      to right,
      #2af2db, 
      #F0F7F4
    )
  }

  .view-projects,
  .contact-me {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    transition: all 0.2s ease;
  }

  .view-projects span,
  .contact-me {
    font-size: var(--text-lg);
    font-weight: 600;
  }

  .view-projects:hover,
  .contact-me:hover {
    cursor: pointer;
    transform: scale(1.1);
  }

  .contact-me {
    background: hsl(from var(--color-background-primary) h s calc(l - 10) / 0.2);
    color: white;
    transition: all 0.2s ease;
  }

  
  /* Ultra-wide screens (1920px+) */
  @media (min-width: 1920px) {
    .hero-container {
      height: 900px;
      background-size: 900px 900px, 900px 900px;
    }

    .title {
      font-size: var(--text-6xl);
    }

    .subtitle {
      font-size: var(--text-4xl);
      width: 40%;
    }
  }

  /* Medium-large desktops (1536px - 1919px) - optimized for 1536x1024 */
  @media (min-width: 1536px) and (max-width: 1919px) {
    .hero-container {
      height: 810px;
      background-size: 600px 600px, 600px 600px;
      background-position: 
        30% 50%,    
        70% 50%;
    }

    .title {
      font-size: calc(var(--text-5xl) * 1.15);
    }

    .subtitle {
      font-size: calc(var(--text-3xl) * 1.05);
      width: 48%;
    }
  }

  /* Large desktops (1440px - 1535px) */
  @media (min-width: 1440px) and (max-width: 1535px) {
    .hero-container {
      height: 850px;
      background-size: 800px 800px, 800px 800px;
    }

    .title {
      font-size: calc(var(--text-5xl) * 1.1);
    }

    .subtitle {
      width: 45%;
    }
  }

  /* Standard desktops (1200px - 1439px) */
  @media (min-width: 1200px) and (max-width: 1439px) {
    .hero-container {
      height: 800px;
    }

    .subtitle {
      width: 55%;
    }
  }

  /* Small desktops/Large tablets (992px - 1199px) */
  @media (min-width: 992px) and (max-width: 1199px) {
    .hero-container {
      height: 700px;
      background-size: 600px 600px, 600px 600px;
      padding: 0 var(--spacing-lg);
    }

    .subtitle {
      width: 65%;
    }
  }

  /* Tablets (768px - 991px) */
  @media (min-width: 768px) and (max-width: 991px) {
    .hero-container {
      height: 600px;
      padding: 0 var(--spacing-xl);
      background-size: 500px 500px, 500px 500px;
    }

    .title {
      font-size: var(--text-4xl);
    }

    .subtitle {
      font-size: var(--text-2xl);
      width: 75%;
    }
  }

  /* Mobile landscape/Small tablets (576px - 767px) */
  @media (min-width: 576px) and (max-width: 767px) {
    .hero-container {
      height: 500px;
      padding: 0 var(--spacing-xl);
      background-size: 450px 450px, 450px 450px;
    }

    .title {
      font-size: var(--text-4xl);
    }

    .subtitle {
      font-size: var(--text-xl);
      width: 80%;
    }

    .call-to-action {
      flex-direction: column;
      gap: var(--spacing-base);
    }
  }

  /* Large mobile (481px - 575px) */
  @media (min-width: 481px) and (max-width: 575px) {
    .hero-container {
      height: 500px;
      padding: 0 var(--spacing-lg);
      gap: var(--spacing-lg);
      background-size: 350px 350px, 350px 350px;
    }

    .title {
      font-size: var(--text-3xl);
      text-align: center;
    }

    .subtitle {
      font-size: var(--text-lg);
      width: 90%;
    }

    .call-to-action {
      flex-direction: column;
      gap: var(--spacing-base);
      width: 90%;
    }
  }

  /* Small mobile (320px - 480px) */
  @media (max-width: 480px) {
    .hero-container {
      height: 500px;
      padding: 0 var(--spacing-lg);
      gap: var(--spacing-lg);
      background-size: 300px 300px, 300px 300px;
    }

    .title {
      font-size: var(--text-3xl);
      text-align: center;
    }

    .title h1 {
      flex-direction: column;
      gap: 0;
    }

    .subtitle {
      font-size: var(--text-lg);
      width: 95%;
    }

    .call-to-action {
      width: 100%;
      flex-direction: column;
      gap: var(--spacing-base);
    }

    .view-projects,
    .contact-me {
      width: 100%;
      padding: var(--spacing-base) var(--spacing-xl);
    }
  }
</style>