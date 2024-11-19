<template>
  <div class="carousel">
    <div class="messages" :style="animationStyle">
      <p v-for="(message, index) in messages" :key="index" class="message">
        {{ message }}
      </p>
    </div>
  </div>
</template>


<script setup>
import { ref, computed, onMounted } from 'vue';

// Array of messages
const messages = ref([
  "The Archive Sale is live. Starting at 20% off. Shop now.",
  "New arrivals are here. Shop the latest styles now.",
  "Limited time offer: Get free shipping on orders over $50."
]);

// Current scroll position
const currentPosition = ref(0);

// Calculate the total width (100vw per message)
const totalWidth = computed(() => messages.value.length * 100);

// Animation style
const animationStyle = computed(() => ({
  transform: `translateX(-${currentPosition.value}vw)`,
  transition: "transform 7s ease-in-out",
}));

// Update position every 20 seconds
onMounted(() => {
  setInterval(() => {
    currentPosition.value = (currentPosition.value + 100) % totalWidth.value;
  }, 10000);
});
</script>



<style scoped>
.carousel {
  position: relative;
  width: 100vw;
  height: 40px; /* Adjust based on desired height */
  overflow: hidden;
  background-color: #000;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.messages {
  display: flex;
  width: max-content; /* Ensure all messages fit horizontally */
}

.message {
  width: 100vw; /* Each message spans the full viewport width */
  text-align: center;
  font-family: "Raleway", sans-serif;
  font-size: 14px;
  letter-spacing: 2px;
  color: #fff;
  flex-shrink: 0; /* Prevent the messages from shrinking */
}
</style>
