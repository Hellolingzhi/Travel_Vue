<template>
  <div>
    <div class="recommend-title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgURL" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.itemTitle}}</p>
          <p class="item-desc">{{item.itemDesc}}</p>
          <a href="javascript:;" class="item-button">查看详情</a>
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
      recommendList: [{
        id: '0001',
        imgURL: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/a3133d16-a13f-4fc3-b774-0e3d45f00cc7.jpg_r_480x320x90_4b7592ea.jpg',
        itemTitle: '南京-北京 5天跟团游',
        itemDesc: '特惠专线|北京纯玩5日游丨可升级酒店+经典景点全含+早定赠天津一日游'
      },
      {
        id: '0002',
        imgURL: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/a3133d16-a13f-4fc3-b774-0e3d45f00cc7.jpg_r_480x320x90_4b7592ea.jpg',
        itemTitle: '南京-北京 5天跟团游',
        itemDesc: '特惠专线|北京纯玩5日游丨可升级酒店+经典景点全含+早定赠天津一日游'
      },
      {
        id: '0003',
        imgURL: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/a3133d16-a13f-4fc3-b774-0e3d45f00cc7.jpg_r_480x320x90_4b7592ea.jpg',
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
  .recommend-title
    line-height: .8rem
    text-algin: center
    background-color: #eee
  .item
    display: flex
    overflow: hidden
    height: 1.9rem
  .item-img-wrapper
    width: 1.7rem
    height: 1.7rem
    padding: .1rem
    .item-img
      width: 100%
      height: 100%
  .item-info
    flex: 1
    min-width: 0
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
    .item-button
      padding: 0 .2rem
      margin-top: .16rem
      background-color: #ff9300
      color: #fff
      line-height: .44rem
      border-radius: .06rem
</style>
