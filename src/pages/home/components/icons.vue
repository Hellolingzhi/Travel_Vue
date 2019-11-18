<template>
  <div class="icons">
    <div class="icon" v-for="item of iconList" :key="item.id">
      <div class="icon-img">
        <img class="icon-img-content" :src="item.imgURL">
      </div>
      <span class="icon-desc">{{item.desc}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/bargainflight.png',
        desc: '民宿客栈民宿客栈民宿客栈民宿客栈'
      },
      {
        id: '0002',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0003',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0004',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0005',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0006',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0007',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0008',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0009',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      },
      {
        id: '0010',
        imgURL: 'https://s.qunarzz.com/homenode/images/touchheader/innBnb.png',
        desc: '机票'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varible.styl'
  @import '~styles/mixins.styl'
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .icon
      overflow: hidden
      float: left
      width: 20%
      height: 0
      padding-bottom: 25%
      .icon-img
        width: 70%
        margin: .2rem auto
        .icon-img-content
          width: 100%
      .icon-desc
        display: block
        color: $darkTextColor
        text-align: center
        ellipsis()
</style>
