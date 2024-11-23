<script setup>
// import { RouterLink, RouterView } from 'vue-router'
import Header from '@/components/Header.vue'
import AnnounceBanner from './components/AnnounceBanner.vue';
import Footer from './components/Footer.vue';

</script>

<template>
  <main>
    <AnnounceBanner />
    <Header />
    <RouterView />
    <Footer />
  </main>
</template>

<style scoped>

</style>
