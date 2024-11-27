<template>
  <main>

    <HomeBanner />

    <div class="home-text-divider">
      <h3>Elevate your lifestyle with a more intelligent, superior wardrobe.</h3>
      <h3>Our range is crafted Sustainably with longevity in mind.</h3>
    </div>


    <!-- First Grid -->
    <div class="cards-container">
      <v-row no-gutters>
        <v-col
          v-for="firstCard in firstCards"
          :key="firstCard.title"
          cols="12"
          sm="4"
          class="pa-3"
        >
          <CardsGrid
            :src="firstCard.src"
            :title="firstCard.title"
            height="530px"
          ></CardsGrid>
        </v-col>

      </v-row>
    </div>

    <div class="home-text-divider">
      <h3>What to Wear Now</h3>
    </div>


    <ProductsGrid />


    <!-- Second Grid -->
    <div class="cards-container">
      <v-row no-gutters>
        <v-col
          v-for="secondCard in secondCards"
          :key="secondCard.title"
          cols="6"
          class="pa-3"
        >
          <CardsGrid
            :src="secondCard.src"
            :title="secondCard.title"
            height="730px"
          ></CardsGrid>
        </v-col>

      </v-row>
    </div>


    <div class="home-text-banner">
      <div class="banner-text-banner-content">
        <h2>The Art of Fewer, Better Choices</h2>
        <p>Opting for quality over quantity means selecting timeless, durable, and responsibly made items. This approach simplifies our lives and fosters a deeper appreciation for our surroundings. Emphasizing longevity and responsible production resonates with a more sustainable and mindful lifestyle.</p>
      </div>
    </div>

    <InstagramGrid />

  </main>
</template>

<script setup>
import HomeBanner from '@/components/HomeBanner.vue';
import CardsGrid from '@/components/CardsGrid.vue';
import ProductsGrid from '@/components/ProductsGrid.vue';
import InstagramGrid from '@/components/InstagramGrid.vue';

import NewArrivals from '@/assets/images/new-arrivals.jpg';
import CasualEdit from '@/assets/images/casual-edit.jpg';
import BestSellers from '@/assets/images/best-sellers.jpg';
import SmartChic from '@/assets/images/smart-chic.jpg';
import Ready2Go from '@/assets/images/ready-to-go.jpg';


const firstCards = [
  {
    title: 'New Arrivals',
    src: NewArrivals,
  },
  {
    title: 'The Casual Edit',
    src: CasualEdit,
  },
  {
    title: 'Best-Sellers',
    src: BestSellers,
  },
];

const secondCards = [
  {
    title: 'The Smart Chic',
    src: SmartChic
  },
  {
    title: 'Ready to Go',
    src: Ready2Go
  }
]

</script>

<style scoped>

  .cards-container {
    margin: auto 28px 10px 28px;
    text-align: start;
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

  .home-text-banner {
    background: rgb(240, 238, 223);
    margin: 30px auto;
  }

  .banner-text-banner-content {
    display: grid;
    gap: 40px;
    place-content: center;
    text-align: center;
    max-width: 720px;
    width: 100%;
    margin: auto;
    height: 450px;
    font-family: "Montserrat", sans-serif;
    color: #636363;
  }

  .banner-text-banner-content h2 {
    font-size: 26px;
    font-weight: 500;
    letter-spacing: 1.5px;
  }

  .banner-text-banner-content p {
    font-size: 16px;
    font-weight: 400;
    letter-spacing: 1px;
  }

</style>
