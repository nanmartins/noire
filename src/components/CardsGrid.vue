<template>
  <main>

    <!-- <v-col
      cols="12"
      sm="4"
      class="pa-3"
    > -->
      <v-sheet class="ma-0 pa-0 card-body">
        <v-img
          :src="src"
          :height="height"
          cover
          class="card-image"
        >
          <div class="card-content">
            <v-card-title class="card-title">{{ title }}</v-card-title>
          </div>
        </v-img>
      </v-sheet>
    <!-- </v-col> -->

  </main>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  src: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  height: {
    type: String,
    default: '530px'
  }
})

</script>


<style scoped>

  .card-body {
    border-radius: 2px;
    overflow: hidden;
  }

  .card-image {
    border-radius: 2px;
    position: relative;
    cursor: pointer;
  }

  .card-content {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 15px;
  }

  .card-title {
    font-family: "Montserrat", sans-serif;
    font-size: 20px;
    font-weight: 400;
    color: rgb(252, 252, 241);
    text-shadow: .5px .5px 1px #565656;
    margin: 0;
  }
</style>
