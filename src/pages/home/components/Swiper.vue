<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20199/76e68eda4ed089c0e5b0ce2367efe428.jpg'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vc/aa/9e/82/14bf523635542806a671763e98.jpg_92.jpg'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/vc/6d/c8/f8/64968edbb09cd02cc08b2c89fa.jpg_92.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background-color: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    .swiper-img
      width: 100%
</style>
