<template>
  <div class="warpper">
    <swiper :options="swiperOptions">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swpier-img" :src="item.imgUrl" :alt="item.imgAlt">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: 0,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/201407/30/b71784bdf6afa1a4f28dfb3467fe0253.jpg_640x276_7f51ed27.jpg',
          imgAlt: '独秀峰王城景区'
        },
        {
          id: 1,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1512/fe/fe08d17ffe7d036b90.water.jpg_640x276_b7d4f2b7.jpg',
          imgAlt: '龙脊梯田'
        }
      ]
    }
  },
  methods: {

  }
}
</script>
<style lang="stylus" scoped>
  .warpper >>> .swiper-pagination-bullet
    background #eee
  .warpper
    width 100%
    height 0
    overflow hidden
    padding-bottom 43.125%
    background-color #eee
    .swpier-img
      width 100%
</style>
