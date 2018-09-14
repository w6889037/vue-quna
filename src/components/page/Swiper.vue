<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
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
  data() {
    return {
      swiperOption: {
          pagination: '.swiper-pagination',
          loop: true
      },
      swiperList:[{
          id:'0001',
          imgUrl:'https://m.tuniucdn.com/fb2/t1/G5/M00/F8/19/Cii-sluHseGIQadxAAJvUm33G7QAAM7OwDyDjkAAm9q98_w640_h0_c0_t0_w640_h0_c0_t0_w640_h0_c0_t0.jpeg'
      },{
          id:'0002',
          imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/81/20/Cii-TFj0m3WII6uwAAFUmD33YmUAAJQzwN-ED8AAVSw27_w640_h0_c0_t0_w640_h0_c0_t0_w640_h0_c0_t0.jpeg'
      },{
          id:'0003',
          imgUrl:'https://m1.tuniucdn.com/fb2/t1/G5/M00/F8/1B/Cii-tFuHslyIPvZYAAOgdWzANZYAAM7PQKxd64AA6CN89_w640_h0_c0_t0_w640_h0_c0_t0_w640_h0_c0_t0.jpeg'
      }]
    };
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


