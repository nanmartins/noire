<template>
  <main>
    <div class="cards-container">
      <v-row no-gutters>
        <v-col
          v-for="card in cards"
          :key="card.title"
          cols="12"
          sm="4"
          class="pa-3"
        >
          <v-sheet class="ma-0 pa-0 card-body">
            <v-img
              :src="card.src"
              height="530px"
              cover
              class="card-image"
            >
              <div class="card-content">
                <v-card-title class="card-title">{{ card.title }}</v-card-title>
              </div>
            </v-img>
          </v-sheet>
        </v-col>
      </v-row>
    </div>
  </main>
</template>

<script setup>
import NewArrivals from '@/assets/images/new-arrivals.jpg';
import CasualEdit from '@/assets/images/casual-edit.jpg';
import BestSellers from '@/assets/images/best-sellers.jpg';

const cards = [
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

</script>


<style scoped>

  .cards-container {
    margin: auto 40px 10px 40px;
    text-align: start;
  }

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
    padding: 20px;
    /* background-color: rgba(0, 0, 0, 0.12); */
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
