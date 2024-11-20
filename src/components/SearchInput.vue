<template>
  <main>
    <div class="search-container d-flex align-center rounded-xl py-1 px-2" :class="{ active: active }">
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
    border: 0.5px solid transparent;
  }

  .search-container.active {
    border: 0.5px solid #868686;
    background: rgb(251, 251, 247);
  }

  input {
    font-family: "Montserrat", sans-serif;
    color: #636363;
    font-size: 13px;
    padding-left: 10px;
  }

  input:focus {
    outline: none;
  }

</style>
