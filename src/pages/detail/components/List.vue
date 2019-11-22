<template>
  <div>
    <div
      class="item"
      v-for="(item, index) of list"
      :key="index"
    >
      <div class="item-title">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
.item-title
  padding: 0 .2rem
  line-height: .8rem
  font-size: .32rem
  .item-title-icon
    position: relative
    top: .07rem
    left: .06rem
    display: inline-block
    width: .36rem
    height: .36rem
    margin-right: .06rem
    background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
    background-size: .4rem 3rem
.item-children
  padding: 0 .2rem
</style>
