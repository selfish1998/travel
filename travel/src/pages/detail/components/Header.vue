<template>
  <div>
    <router-link tag="div" to="/" class="header-abs" v-show="showAbs">
      <div class="iconfont header-abs-icon">&#xe624;</div>
    </router-link>
    <router-link tag="div" to="/" class="header-fixed" v-show="showFix" :style="opacityStyle">
      景点详情
      <div class="iconfont header-fixed-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  components: {
  },
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  computed: {
    showFix () {
      return (!this.showAbs)
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop || document.body.scrollTop || window.pageYOffset
      if (top > 60) {
        let opacity = top / 140
        opacity = (opacity > 1) ? 1 : opacity
        this.opacityStyle = {
          opacity
        }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroy () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header-abs
    position absolute
    left .2rem
    top .2rem
    width .8rem
    height .8rem
    line-height .8rem
    text-align center
    border-radius .4rem
    background rgba(0, 0, 0, 0.8)
    .header-abs-icon
      color #fff
      font-size .4rem
  .header-fixed
    position fixed
    z-index 2
    top 0
    left 0
    right 0
    height $headerHeight
    line-height $headerHeight
    text-align center
    color #fff
    background-color $bgColor
    font-size .32rem
    .header-fixed-back
      position absolute
      color #fff
      width .64rem
      top 0
      left 0
      text-align center
      font-size .4rem
</style>
