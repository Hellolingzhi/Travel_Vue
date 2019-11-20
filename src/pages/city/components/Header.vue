<template>
  <div class="header">
    <router-link to="/">
      <span class="iconfont back-index">&#xe6db;</span>
    </router-link>
    城市列表
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
.header
  position: relative
  height: .86rem
  line-height: .86rem
  text-align: center
  font-size: .32rem
  color: #fff
  background-color: $bgColor
  .back-index
    position: absolute
    left: .4rem
    top: 0
    font-size: .4rem
    color: #fff
</style>
