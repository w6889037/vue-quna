<template>
  <div>
      <home-header></home-header>
      <home-swiper :swiperList="swiperList"></home-swiper>
      <icon></icon>
      <home-recommend :recommendList="recommendList"></home-recommend>
      <home-weekend :weekendList="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from "./page/Header";
import HomeSwiper from "./page/Swiper";
import Icon from "./page/Icon";
import HomeRecommend from "./page/Recommend";
import HomeWeekend from "./page/Weekend";
import axios from "axios";

export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    Icon,
    HomeRecommend,
    HomeWeekend
  },
  data() {
    return {
      recommendList: [],
      swiperList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo() {
      axios
        .get("/api/home/list")
        .then(this.getHomeInfoSuccess);
    },
    getHomeInfoSuccess(res) {
      this.recommendList = res.data.recommendList
      this.swiperList = res.data.swiperList
      this.weekendList = res.data.weekendList
    }
  },
  mounted() {
    this.getHomeInfo();
  }
};
</script>
