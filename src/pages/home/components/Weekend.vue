<template>
  <div>
    <div class="weekend-title">
      周末去哪儿
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgURL" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.itemTitle}}</p>
          <p class="item-desc">{{item.itemDesc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgURL: 'https://imgs.qunarzz.com/p/tts9/1806/52/39318582f0307502.jpg_r_390x260x90_c6d0d7fa.jpg',
        itemTitle: '南京-北京 5天跟团游',
        itemDesc: '特惠专线|北京纯玩5日游丨可升级酒店+经典景点全含+早定赠天津一日游'
      },
      {
        id: '0002',
        imgURL: 'https://imgs.qunarzz.com/p/tts9/1806/52/39318582f0307502.jpg_r_390x260x90_c6d0d7fa.jpg',
        itemTitle: '南京-北京 5天跟团游',
        itemDesc: '特惠专线|北京纯玩5日游丨可升级酒店+经典景点全含+早定赠天津一日游'
      },
      {
        id: '0003',
        imgURL: 'https://imgs.qunarzz.com/p/tts9/1806/52/39318582f0307502.jpg_r_390x260x90_c6d0d7fa.jpg',
        itemTitle: '南京-北京 5天跟团游',
        itemDesc: '特惠专线|北京纯玩5日游丨可升级酒店+经典景点全含+早定赠天津一日游'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varible.styl'
  @import '~styles/mixins.styl'
  .weekend-title
    line-height: .8rem
    text-algin: center
    background-color: #eee
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    color: $darkTextColor
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
