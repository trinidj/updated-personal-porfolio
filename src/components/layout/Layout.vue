<script setup>
  import Header from '@/components/shared/Header.vue';
  import Footer from '@/components/shared/Footer.vue';
</script>

<template>
  <body>
    <Header />
    <main>
      <slot />
    </main>
    <Footer />
  </body>
</template>

<style scoped>

</style>