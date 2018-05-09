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
        imgUrl: 'https://mall.s.maizuo.com/a373113ee66ca2590c0c0dc5b1eaf444.jpg?x-oss-process=image/quality,Q_70'
      }, {
        id: '0002',
        imgUrl: 'https://mall.s.maizuo.com/572920cba93d787b9c56729e65d8fda7.jpg?x-oss-process=image/quality,Q_70'
      }, {
        id: '0003',
        imgUrl: 'https://mall.s.maizuo.com/59a439c3a59322929cb328fd2fe482fe.jpg?x-oss-process=image/quality,Q_70'
      }, {
        id: '0004',
        imgUrl: 'https://mall.s.maizuo.com/d042d3f4da3f615eeb6a018a61a43ecc.jpg?x-oss-process=image/quality,Q_70'
      }, {
        id: '0005',
        imgUrl: 'https://mall.s.maizuo.com/bfb5c2fca4df9a0e2d06256e300d29bf.jpg?x-oss-process=image/quality,Q_70'
      }, {
        id: '0006',
        imgUrl: 'https://mall.s.maizuo.com/c2ea9ed51a31bb3f864b6b020da0d000.jpg?x-oss-process=image/quality,Q_70'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  // >>>穿透,只要.wrapper下出现.swiper-pagination-bullet-active,就用此样式,不受scoped的限制
  //样式实际上在Swiper中,并不在当前组件内
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    // 高度相对于宽度会自动撑开31.25%
    padding-bottom: 56%
    background: #eee
    .swiper-img
      width: 100%
</style>
