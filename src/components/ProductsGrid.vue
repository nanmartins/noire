<template>
  <main>

    <v-row
      class="products-container pb-12"
      no-gutters
    >
      <v-col
        v-for="product in products"
        :key="product.title"
        class="products-content"
      >
        <v-sheet>
          <v-img :src="product.img" height="340px" cover></v-img>
          <div class="product-text">
            <p>{{ product.title }}</p>
            <p class="product-price">{{ product.price }}</p>
          </div>
        </v-sheet>
      </v-col>
    </v-row>

  </main>
</template>


<script setup>
import Style01 from '@/assets/images/style01.jpg';
import Style02 from '@/assets/images/style02.jpg';
import Style03 from '@/assets/images/style03.jpg';
import Style04 from '@/assets/images/style04.jpg';
import Style05 from '@/assets/images/style05.jpg';

const products = [
  {
    img: Style01,
    title: 'Handmade Crochet Poncho',
    price: '£109',
  },
  {
    img: Style02,
    title: 'Cupro Blend Shirt',
    price: '£99',
  },
  {
    img: Style03,
    title: 'Vegan Leather Oxford Shoes',
    price: '£299',
  },
  {
    img: Style04,
    title: 'Mesh Sneakers - Lace Up',
    price: '£239',
  },
  {
    img: Style05,
    title: 'Soft Bomber Jacket',
    price: '£169',
  },
]

</script>


<style scoped>

  .products-container {
    gap: 20px;
    margin: auto 40px;
  }

  .products-content {
    width: 300px;
  }

  .v-sheet {
    background: transparent;
  }

  .product-text {
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
    font-weight: 600;
    color: #636363;
    padding: 15px 0;
  }

  .product-price {
    font-size: 14px;
    padding-top: 3px;
  }

</style>
