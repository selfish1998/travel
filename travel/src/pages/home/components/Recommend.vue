<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" :alt="item.title">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/201403/10/e68de0a0c26d0be47dd442595a176a2f.jpg_200x200_d5383e90.jpg',
          title: '野人谷漂流',
          desc: '🔥好评如潮，小伙伴热推景点~'
        },
        {
          id: '0002',
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/201403/21/1ee59d4e8f0e2b71eb881fdf62e17f45.jpg_200x200_ae03f711.jpg',
          title: '野人谷景区',
          desc: '👍小伙伴们都收藏了，去看看吧~'
        },
        {
          id: '0003',
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1906/65/6523eb12470f1a27a3.img.jpg_200x200_36908881.jpg',
          title: '十万大山温泉',
          desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height .7rem
    text-indent .2rem
    margin-top .2rem
    background-color #ccc
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        margin-top .16rem
        color #fff
        line-height .44rem
        background-color #ff9300
        padding 0 .2rem
        border-radius .06rem
</style>
