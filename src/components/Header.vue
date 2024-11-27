<template>
  <header>
    <div class="logo-nav">
      <img src="../assets/images/noire-logo.png" alt="">
      <nav>
        <a href="">Shop</a>
        <a href="">New Arrivals</a>
        <a href="">Sales</a>
      </nav>
    </div>


    <div>
      <SearchInput />
      <a href="">Stores</a>
      <UserIcon />
      <FavoriteIcon />
      <CartIcon />
    </div>
  </header>
</template>

<script setup>
import UserIcon from '@/assets/icons/UserIcon.vue';
import FavoriteIcon from '@/assets/icons/FavoriteIcon.vue';
import CartIcon from '@/assets/icons/CartIcon.vue';
import SearchInput from './SearchInput.vue';

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
  gap: 24px;
}

.logo-nav {
  gap: 40px;
}

nav {
  display: flex;
  gap: 30px;
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


</style>
