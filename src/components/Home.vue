<template>
  <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHeader from "./page/Header"
import HomeSwiper from "./page/Swiper"
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper
  }
};
</script>
