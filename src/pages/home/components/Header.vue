<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe6db;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe6e1;</span>输入城市/景点/游玩/主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont">&#xe600;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varible.styl'
.header
  display: flex
  line-height: .86rem
  background-color: $bgColor
  color: #fff
  .iconfont
    display: inline-block
    font-size: .35rem
  .header-left
    width: .64rem
    float: left
    .iconfont
      margin-left: .2rem
  .header-right
    float: right
    width: 1.24rem
    text-align: center
    color: #fff
    .iconfont
      font-size: .24rem
  .header-input
    flex: 1
    height: .64rem
    margin: .12rem 0 0 .2rem
    background-color: #fff
    color: #ccc
    line-height: .64rem
    border-radius: .1rem
    .iconfont
      margin-right: .1rem
</style>
