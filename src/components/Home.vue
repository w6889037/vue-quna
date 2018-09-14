<template>
  <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <icon></icon>
  </div>
</template>

<script>
import HomeHeader from "./page/Header"
import HomeSwiper from "./page/Swiper"
import Icon from "./page/Icon"
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    Icon
  }
};
</script>
