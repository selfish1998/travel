<template>
  <div class="warpper">
    <swiper :options="swiperOptions" v-if="showSwiper">
    <swiper-slide v-for="item of list" :key="item.id">
      <img class="swpier-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
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
    padding-bottom 31.25%
    background-color #eee
    .swpier-img
      width 100%
</style>
