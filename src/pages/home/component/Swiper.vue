<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
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
        imgUrl: 'http://pic112.nipic.com/file/20161012/10473926_212348452000_2.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://pic18.nipic.com/20111129/2229195_083700745000_2.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  // >>>穿透,只要.wrapper下出现.swiper-pagination-bullet-active,就用此样式,不受scoped的限制
  //样式实际上在Swiper中,并不在当前组件内
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    // 高度相对于宽度会自动撑开31.25%
    padding-bottom: 67%
    background: #eee
    .swiper-img
      width: 100%
</style>
