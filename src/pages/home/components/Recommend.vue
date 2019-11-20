<template>
  <div>
    <div class="recommend-title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommend" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <a href="javascript:;" class="item-button">查看详情</a>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommend: Array
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
