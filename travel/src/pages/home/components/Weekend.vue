<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-warpper">
          <img class="item-img" :src="item.imgUrl" :alt="item.title">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  },
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1509/b0/83481d0d95a39b.jpg_r_640x214_7dc3d605.jpg',
          title: '秘境广西',
          desc: '想知道真实的桂林之景和作者笔下的桂林有差别吗？快来揭晓你心中那个未知之谜吧'
        },
        {
          id: '0002',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1507/98/1b8d44654e4235.jpg_r_640x214_f82c5d33.jpg',
          title: '广西热门取景地',
          desc: '不走寻常路，到明星们走过的地儿走走逛逛，感受这里的青山绿水好风光'
        },
        {
          id: '0003',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1507/20/065ee2c0ca26d4.jpg_r_640x214_a70e0f1b.jpg',
          title: '广西最刺激漂流TOP10',
          desc: '漂流，漂流，这个夏天就是要玩点刺激的'
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
    background-color #ccc
  .item-img-warpper
    overflow hidden
    height 0
    padding-bottom 38.0107%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .28rem
      ellipsis()
    .item-desc
      line-height .4rem
      font-size: .24rem;
      color #ccc
      ellipsis()

</style>
