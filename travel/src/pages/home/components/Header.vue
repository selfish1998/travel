<template>
  <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
      </div>
      <router-link to="./city">
        <div class="header-right">
          {{city}}
          <span class="iconfont arrow-icon">&#xe600;</span>
        </div>
      </router-link>

  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles'
  .header
    display flex
    line-height $headerHeight
    background-color $bgColor
    color #fff
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      background #fff
      height .62rem
      padding-left .2rem
      line-height .62rem
      margin-top .12rem
      margin-left .2rem
      border-radius .1rem
      color #ccc
    .header-right
      min-width 1.04rem
      float right
      padding 0 .1rem
      text-align center
      color #fff
      .arrow-icon
        font-size .24rem
        margin-left -.04rem
</style>
