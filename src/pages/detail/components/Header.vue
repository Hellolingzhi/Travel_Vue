<template>
  <div>
    <transition>
      <router-link
        tag="div"
        to="/"
        class="header-abs"
        v-if="showAbs"
      >
        <span class="iconfont">&#xe6db;</span>
      </router-link>
      <div class="header-fixed" v-else>
        <router-link to='/'>
          <span class="iconfont">&#xe6db;</span>
        </router-link>
        景点详情
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true
    }
  },
  methods: {
    handleScroll () {
      console.log('scroll')
      const top = document.documentElement.scrollTop
      if (top > 60) {
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    console.log(1)
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    console.log(2)
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
.header-abs
  position: fixed
  z-index: 999
  left: .25rem
  top: .1rem
  width: .7rem
  height: .7rem
  line-height: .7rem
  background-color: #000
  border-radius: 50%
  .iconfont
    display: block
    color: #ccc
    font-size: .4rem
    text-align: center
.header-fixed
  position: fixed
  z-index: 999
  top: 0
  left: 0
  right: 0
  height: $headerHeight
  line-height: $headerHeight
  text-align: center
  font-size: .32rem
  color: #fff
  background-color: $bgColor
  .iconfont
    position: absolute
    left: .4rem
    top: 0
    font-size: .4rem
    color: #fff
.v-enter
.v-leave-to
  opacity: 0
.v-enter-active
.v-leave-active
  transition: all .8s;
</style>
