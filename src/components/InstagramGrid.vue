<template>
  <main>
    <h3>Shop Instagram</h3>


    <v-row
      class="instagram-grid pb-10"
      no-gutters
    >
      <v-col
        v-for="insta in instaPages"
        :key="insta.img"
        class="insta-content"
      >
        <v-sheet>
          <v-img :src="insta.img" height="300px" cover class="insta-image-container">
            <div class="overlay">
              <InstagramIcon class="icon" />
            </div>
          </v-img>
        </v-sheet>
      </v-col>
    </v-row>


  </main>
</template>


<script setup>
import InstagramIcon from '@/assets/icons/InstagramIcon.vue';

const instaPages = [
  {
    img: 'https://images.unsplash.com/photo-1588358641419-458f7616cbf2?q=80&w=3087&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    src: '',
  },
  {
    img: 'https://images.unsplash.com/photo-1656258762138-f834870c29b0?q=80&w=3043&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    src: '',
  },
  {
    img: 'https://images.unsplash.com/photo-1619086311112-f70682597d32?q=80&w=3087&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    src: '',
  },
  {
    img: 'https://images.unsplash.com/photo-1728994704247-c6f7e37377f7?q=80&w=3087&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    src: '',
  },
  {
    img: 'https://images.unsplash.com/photo-1496440737103-cd596325d314?q=80&w=3087&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    src: '',
  },
]

</script>


<style scoped>

  .instagram-grid {
    gap: 20px;
    margin: auto 30px;
  }

  h3 {
    text-align: center;
    font-family: "Montserrat", sans-serif;
    font-size: 20px;
    font-weight: 500;
    letter-spacing: 1.5px;
    color: #636363;
    padding: 30px 0 70px 0;
  }

  .insta-image-container {
    position: relative;
    overflow: hidden;
    cursor: pointer;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
  }

  .insta-image-container:hover .overlay {
    opacity: 1;
  }

</style>
