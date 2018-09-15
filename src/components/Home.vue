<template>
  <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <icon></icon>
      <home-recommend></home-recommend>
      <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from "./page/Header"
import HomeSwiper from "./page/Swiper"
import Icon from "./page/Icon"
import HomeRecommend from "./page/Recommend"
import HomeWeekend from "./page/Weekend"
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    Icon,
    HomeRecommend,
    HomeWeekend
  }
};
</script>
