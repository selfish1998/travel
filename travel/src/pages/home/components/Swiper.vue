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
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1507/9f/f8dde5c968f8ac.jpg_r_640x214_83194a9b.jpg',
          imgAlt: '广西最美瀑布'
        },
        {
          id: 1,
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1507/12/0f76178631aa56.jpg_r_640x214_b3adf11d.jpg',
          imgAlt: '广西水上乐园哪家强'
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
    padding-bottom 37.6761%
    background-color #eee
    .swpier-img
      width 100%
</style>
