<template>
    <div class="wrapper">
        <swiper :options="swiperOption" v-if="showSwiper">
            <!-- slides -->
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img :src="item.imgUrl" class="swiper-img">
            </swiper-slide>
            <!-- <swiper-slide>I'm Slide 4</swiper-slide>
            <swiper-slide>I'm Slide 5</swiper-slide>
            <swiper-slide>I'm Slide 6</swiper-slide>
            <swiper-slide>I'm Slide 7</swiper-slide> -->
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
            <!-- <div class="swiper-button-prev" slot="button-prev"></div>
            <div class="swiper-button-next" slot="button-next"></div>
            <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
        </swiper>
    </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  props:{
    swiperList: Array
  },
  data() {
    return {
      swiperOption: {
          pagination: '.swiper-pagination',
          loop: true
      }
    };
  },
  computed: {
      showSwiper() {
          return this.swiperList.length
      }
  }
};
</script>

<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff
.wrapper
    overflow: hidden
    width: 100%
    padding-bottem: 31.25%
    .swiper-img
        width: 100%

</style>


