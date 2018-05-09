<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [{
        id: '001',
        imgUrl: 'https://mall.s.maizuo.com/2098a3fbbb398b2650810475afa2fc23.jpg?x-oss-process=image/quality,Q_70',
        desc: '9.9拼团9.9拼团9.9拼团9.9拼团'
      }, {
        id: '002',
        imgUrl: 'https://mall.s.maizuo.com/21760cfcf42efbdb7dd09159921002fb.jpg?x-oss-process=image/quality,Q_70',
        desc: '居家'
      }, {
        id: '003',
        imgUrl: 'https://mall.s.maizuo.com/dfafbc3e5f4a510fdbba396385e36d10.jpg?x-oss-process=image/quality,Q_70',
        desc: '餐厨'
      }, {
        id: '004',
        imgUrl: 'https://mall.s.maizuo.com/84fc64e5784540474b7427e2e85f4526.jpg?x-oss-process=image/quality,Q_70',
        desc: '食品'
      }, {
        id: '005',
        imgUrl: 'https://mall.s.maizuo.com/cbfe5aafcb9e6c2198064f53b55d1729.jpg?x-oss-process=image/quality,Q_70',
        desc: '水果'
      }, {
        id: '006',
        imgUrl: 'https://mall.s.maizuo.com/5d208b53db490f702b616ece6e612c80.jpg?x-oss-process=image/quality,Q_70',
        desc: '小家电'
      }, {
        id: '007',
        imgUrl: 'https://mall.s.maizuo.com/94f2a70c74010dee0bd4f37e243e7b09.jpg?x-oss-process=image/quality,Q_70',
        desc: '跨境'
      }, {
        id: '008',
        imgUrl: 'https://mall.s.maizuo.com/019be663c67b5ea50849573273e69b68.jpg?x-oss-process=image/quality,Q_70',
        desc: '洗护'
      }, {
        id: '009',
        imgUrl: 'https://mall.s.maizuo.com/2098a3fbbb398b2650810475afa2fc23.jpg?x-oss-process=image/quality,Q_70',
        desc: '9.9包邮'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        // 当前下标的图标应该显示在第几页
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          // 如果当前数组不存在,建立一个新数组,把相应的push进去
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon
    position: relative
    overflow: hidden
    float: left
    width: 25%
    hieght: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      .icon-img-content
        display:block
        margin: 0 auto
        height: 100%
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: 0.44rem
      line-height: 0.44rem
      text-align: center
      color: $darkTextColor
      ellipsis()

</style>
