<template>
  <div>
    <div class="weekend-title">
      周末去哪儿
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of weekend" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img">
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
    weekend: Array
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
    padding-bottom: 37.09%
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
