<script setup>
  import ServiceCard from '@/components/ui/ServiceCard.vue';
  import { Code2, Palette, Lightbulb } from 'lucide-vue-next';

  const services = [
    {
      id: 1,
      title: "Front-end Development",
      description: "Expert in React, TypeScript, Next.js, and modern CSS frameworks. Building responsive, performant user interfaces with clean code.",
      icon: Code2
    },
    {
      id: 2,
      title: "UI/UX Design",
      description: "Creating intuitive and visually appealing user interfaces with attention to detail and user experience best practices.",
      icon: Palette
    },
    {
      id: 3,
      title: "Creative Solutions",
      description: "Innovative problem-solving approach to complex technical challenges, turning ideas into functional digital experiences.",
      icon: Lightbulb
    }
  ]
</script>

<template>
  <section id="about-section">
    <div class="about-container">
      <div class="title">
        <h2>About Me</h2>
        <p>
          Passionate front-end developer specializing in React, TypeScript, and modern web     technologies to create exceptional user experiences.
        </p>
      </div>

      <div class="grid">
        <div class="about-content">
          <h3>Crafting User Experiences</h3>
          <p>
            I'm a front-end developer with over 5 years of experience creating stunning, responsive web applications. My journey started with HTML and CSS and has evolved into mastering modern frameworks like React, Vue, and cutting-edge tools.

            I believe that exceptional user interfaces are born from the perfect blend of beautiful design and flawless functionality. Every component I build focuses on user experience, performance, and maintainable code architecture.

            When I'm not coding, you'll find me staying up-to-date with the latest front-end trends, experimenting with new CSS techniques, or perfecting my workflow with the newest development tools.
          </p>
        </div>

        <div class="services">
          <ServiceCard 
            v-for="service in services"
            :key="service.id"
            :title="service.title"
            :description="service.description"
            :icon="service.icon"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .about-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: var(--spacing-5xl);
    justify-content: center;
    background: hsl(from var(--color-background-primary) h s calc(l - 2));
    margin: 0 auto;
  }

  .title {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: var(--spacing-7xl);
    padding-bottom: 0;
  }

  .title h2 {
    font-size: var(--text-5xl);
    background-image: linear-gradient(to right, #00eeff, #00949e);
    margin-bottom: var(--spacing-base);

    background-clip: text;
    -webkit-background-clip: text; 

    color: transparent;
    -webkit-text-fill-color: transparent; 
  }

  .title p {
    font-size: var(--text-2xl);
    font-weight: 600;
    width: 60%;
    text-align: center;
    color: hsl(from var(--color-text-primary) h s l / 0.5);
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: var(--spacing-4xl);
    padding: var(--spacing-7xl);
    padding-top: 0;
  }

  .services {
    display: flex;
    flex-direction: column;
    gap: var(--spacing-base);
  }
</style>