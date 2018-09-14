<template>
  <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <icon></icon>
      <home-recommend></home-recommend>
  </div>
</template>

<script>
import HomeHeader from "./page/Header"
import HomeSwiper from "./page/Swiper"
import Icon from "./page/Icon"
import HomeRecommend from "./page/Recommend"
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    Icon,
    HomeRecommend
  }
};
</script>
