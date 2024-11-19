<script setup>
// import { RouterLink, RouterView } from 'vue-router'
import Header from '@/components/Header.vue'
import AnnounceBanner from './components/AnnounceBanner.vue';

</script>

<template>
  <main>
    <AnnounceBanner />
    <Header />
    <RouterView />
  </main>
</template>

<style scoped>

</style>
