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
  </main>
</template>

<script setup>
import HomeBanner from '@/assets/images/home-banner.jpg';

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
    object-fit: cover;
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
    background-color: rgba(252, 252, 241);
    color: #636363;
    border: none;
    cursor: pointer;
  }

  button:hover {
    color: #000;
  }


  @media screen and (max-width: 800px) {
    .banner-container {
      height: auto;
    }

    img {
      aspect-ratio: 3/4;
      object-fit: cover;
    }

    .banner-text {
      bottom: 12%;
      left: 7%;
      max-width: 80%;
    }

    .banner-text h2 {
      font-size: 20px;
    }

    button {
      font-size: 16px;
      padding: 8px 20px;
    }
  }

</style>
