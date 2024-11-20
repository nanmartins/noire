<template>
  <v-carousel
    cycle
    hide-delimiters
    interval="10000"
    height="45px"
  >
    <v-carousel-item
      v-for="(message, i) in messages"
      :key="i"
    >
      <v-sheet
        height="100%"
        color="#000000"

      >
        <div class="d-flex fill-height justify-center align-center">
          <div class="message">
            {{ message }}
          </div>
        </div>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script setup>
import { ref } from 'vue';

const messages = ref([
  "The Archive Sale is live. Starting at 20% off. Shop now.",
  "New arrivals are here. Shop the latest styles now.",
  "Limited time offer: Get free shipping on orders over £50."
]);

</script>



<style scoped>

.message {
  font-family: "Raleway", sans-serif;
  font-size: 14px;
  letter-spacing: 2px;
  color: #fff;
}
</style>
