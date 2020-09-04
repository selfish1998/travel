<template>
  <div class="icons">
    <swiper >
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" :alt="item.imgAlt">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>

      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>

  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [
        {
          id: '0001',
          imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
          imgAlt: '景点门票',
          desc: '景点门票'
        },
        {
          id: '0002',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          imgAlt: '周边游hot',
          desc: '周边游hot'
        },
        {
          id: '0003',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          imgAlt: '德天瀑布',
          desc: '德天瀑布'
        },
        {
          id: '0004',
          imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
          imgAlt: '景点门票',
          desc: '景点门票'
        },
        {
          id: '0005',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          imgAlt: '周边游hot',
          desc: '周边游hot'
        },
        {
          id: '0006',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          imgAlt: '德天瀑布',
          desc: '德天瀑布'
        },
        {
          id: '0007',
          imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
          imgAlt: '景点门票',
          desc: '景点门票'
        },
        {
          id: '0008',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          imgAlt: '周边游hot',
          desc: '周边游hot'
        },
        {
          id: '0009',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
          imgAlt: '泡温泉',
          desc: '泡温泉'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icon
    position relative
    width 25%
    float left
    height 0
    overflow hidden
    padding-bottom 25%
    .icon-img
      position absolute
      top 0
      left 0
      right 0
      bottom .44rem
      box-sizing border-box
      padding .1rem
      .icon-img-content
        display block
        height 100%
        margin 0 auto
    .icon-desc
      position absolute
      bottom 0
      left 0
      right 0
      height  .44rem
      line-height .44rem
      color $darkTextColor
      text-align center
      ellipsis()
</style>
