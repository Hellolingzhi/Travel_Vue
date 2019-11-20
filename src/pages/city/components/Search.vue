<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="请输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
.search
  height: .72rem
  padding: 0 .1rem
  background-color: $bgColor
  .search-input
    box-sizing: border-box
    width: 100%
    padding: 0 .1rem
    height: .6rem
    line-height: .6rem
    text-alie: center
    color: #666
    border-radius: .06rem
</style>
