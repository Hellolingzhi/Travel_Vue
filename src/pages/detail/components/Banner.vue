<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" alt="">
      <div class="banner-info">
        <p class="banner-title">
          {{this.sightName}}
        </p>
        <div class="banner-number">
          <span class="iconfont">&#xe61a;</span>
          {{this.gallaryImgs.length}}
        </div>
      </div>
    </div>
    <common-gallary :imgs="gallaryImgs" v-show="showGallary" @closeGallary="handleGarrayClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary.vue'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false
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
