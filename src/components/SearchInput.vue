<template>
  <main>
    <div class="search-container d-flex align-center rounded py-1 px-2" :class="{ active: active }">
      <input v-show="active" type="text" placeholder="Search">
      <SearchIcon @click="active = !active"/>
    </div>

  </main>

</template>

<script setup>
import { ref } from 'vue';
import SearchIcon from '@/assets/icons/SearchIcon.vue';

const active = ref(false);



</script>

<style scoped>

  .search-container {
    display: flex;
    align-items: center;
  }

  .search-container.active {
    border: .7px solid #636363;
    background: #fff;
  }

  input:focus {
    outline: none;
  }

  /* .active {
    border: .7px solid #636363;
    background: #fff;
  } */

</style>
