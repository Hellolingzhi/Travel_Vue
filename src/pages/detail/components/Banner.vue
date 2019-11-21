<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="https://imgs.qunarzz.com/sight/p0/1603/85/85aa0c000578a01e90.water.jpg_710x360_4621c512.jpg" alt="">
      <div class="banner-info">
        <p class="banner-title">庭院错落，花木为胜，天下园林之典范</p>
        <div class="banner-number">
          <span class="iconfont">&#xe61a;</span>
          30
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @closeGallary="handleGarrayClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary.vue'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_800x800_70debc93.jpg', 'http://img1.qunarzz.com/sight/p0/1709/76/7691528bc7d7ad3ca3.img.png_800x800_9ef05ee7.png']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGarrayClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 50.7%
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    bottom: 0
    left: 0
    right: 0
    line-height: .6rem
    color: #fff
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
    .banner-title
      flex: 1
      font-size: .3rem
      padding: 0 .2rem
    .banner-number
      height: .32rem
      margin-top: .14rem
      padding: 0 .4rem
      font-size: .24rem
      line-height: .32rem
      border-radius: .2rem
      background: rgba(0, 0, 0, .75)
      .iconfont
        font-size: .24rem
</style>
