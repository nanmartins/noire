<template>
  <main>

    <header>

      <div class="mobile-nav">
        <HamburgerIcon />

      </div>

      <div class="logo-nav">
        <img src="../assets/images/noire-logo.png" alt="">

        <nav>
          <a href="">Shop</a>
          <a href="">New Arrivals</a>
          <a href="">Sales</a>
        </nav>
      </div>


      <div>
        <SearchIcon @click="searchContainer = true" class="svg-icons"/>
        <a href="" class="stores-link">Stores</a>
        <UserIcon class="user-icon" />
        <FavoriteIcon class="svg-icons" />
        <CartIcon class="svg-icons" />
      </div>
    </header>

    <div class="search-container" :class="{ active: searchContainer }">
      <SearchIcon />
      <input v-show="searchContainer" type="text" placeholder="Search...">
      <CloseIcon @click="searchContainer = !searchContainer" />
    </div>

  </main>
</template>

<script setup>
import { ref } from 'vue';
import UserIcon from '@/assets/icons/UserIcon.vue';
import FavoriteIcon from '@/assets/icons/FavoriteIcon.vue';
import CartIcon from '@/assets/icons/CartIcon.vue';
import SearchIcon from '@/assets/icons/SearchIcon.vue';
import CloseIcon from '@/assets/icons/CloseIcon.vue';
import HamburgerIcon from '@/assets/icons/HamburgerIcon.vue';


const searchContainer = ref(false);

</script>

<style scoped>

  header {
    display: flex;
    justify-content: space-between;
    padding: 25px 30px;
  }

  header > div {
    display: flex;
    align-items: center;
    gap: 25px;
  }

  .logo-nav {
    gap: 40px;
  }

  .logo-nav nav {
    display: flex;
    gap: 25px;
  }

  a {
    text-decoration: none;
    color: #636363;
    font-family: "Montserrat", sans-serif;
    font-weight: 500;
  }

  a:hover {
    color: #000000;
  }

  img {
    width: 120px;
  }


  /* SEARCH CONTAINER */
  .search-container {
    display: none;
    justify-content: center;
    align-items: center;
    padding: 5px 40px 10px 40px;
  }

  .search-container.active {
    display: flex;
    gap: 20px;
  }

  .search-container input {
    padding: 5px;
    width: 100%;
    font-family: "Montserrat", sans-serif;
    color: #636363;
    border-bottom: 0.5px solid #bbbbbb;
    font-size: 14px;
  }

  .search-container input:focus {
    outline: none;
  }

  .mobile-nav {
    display: none;
  }


  @media screen and (max-width: 800px) {

    header {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      padding: 15px;
    }

    header > div:last-child {
      position: absolute;
      right: 15px;
      display: flex;
      align-items: center;
      gap: 15px;
    }

    img {
      margin: 0 auto;
      width: 90px;
    }

    .logo-nav nav, .user-icon, .stores-link {
      display: none;
    }

    .mobile-nav {
      display: flex;
      position: absolute;
      left: 15px;
    }

    .svg-icons {
      height: 18px;
      width: 18px;
    }

  }

</style>
