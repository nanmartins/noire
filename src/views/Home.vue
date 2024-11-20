<template>
  <main>
    <div class="banner-container">
      <img :src="HomeBanner" alt="Home Banner">
      <div class="banner-text">
        <h2>Elevate Your Style</h2>
        <h2>Timeless Fashion, Sustainable Choices</h2>
        <button>Shop Now</button>
      </div>
    </div>

    <div class="home-text-divider">
      <h3>Elevate your lifestyle with a more intelligent, superior wardrobe.</h3>
      <h3>Our range is crafted Sustainably with longevity in mind.</h3>
    </div>

    <CardsGrid />

    <div class="home-text-divider">
      <h3>What to Wear Now</h3>
    </div>

    <ProductsGrid />

  </main>
</template>

<script setup>
import HomeBanner from '@/assets/images/home-banner.jpg';
import CardsGrid from '@/components/CardsGrid.vue';
import ProductsGrid from '@/components/ProductsGrid.vue';

</script>

<style scoped>

  .banner-container {
    position: relative;
    width: 100%;
    height: 100%;
  }

  img {
    width: 100%;
    height: auto;
  }

  .banner-text {
    position: absolute;
    bottom: 15%;
    left: 7%;
    color: rgb(252, 252, 241);
    word-wrap: break-word;
    max-width: 30%;
  }

  .banner-text h2 {
    font-family: "Montserrat", sans-serif;
    font-size: 26px;
    font-weight: 500;
    letter-spacing: 1.5px;
  }

  button {
    margin-top: 15px;
    padding: 10px 25px;
    font-family: "Raleway", sans-serif;
    font-size: 18px;
    font-weight: 400;
    background-color: rgba(252, 252, 241, 0.832);
    color: #636363;
    border: none;
    border-radius:1px;
    cursor: pointer;
    box-shadow: 0 2px 2px rgba(32, 32, 32, 0.2);
  }

  button:hover {
    color: #000;
  }

  .home-text-divider {
    text-align: left;
    padding: 60px 40px;
  }

  .home-text-divider h3 {
    font-family: "Montserrat", sans-serif;
    font-size: 22px;
    font-weight: 400;
    letter-spacing: 1.2px;
    color: #636363;
    margin-left: 40px;
  }

</style>
