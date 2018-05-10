<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '001',
          imgUrl: 'https://mall.s.maizuo.com/f3fb14bcc57fa2c18b9c4b72d49c4f4f.png?x-oss-process=image/quality,Q_70',
          title: '标题标题标题标题标题标题标题标题标题标题标题标题标题标题标题',
          desc: '内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容'
        }, {
          id: '002',
          imgUrl: 'https://mall.s.maizuo.com/f3fb14bcc57fa2c18b9c4b72d49c4f4f.png?x-oss-process=image/quality,Q_70',
          title: '标题标题标题',
          desc: '内容内容内容'
        }, {
          id: '003',
          imgUrl: 'https://mall.s.maizuo.com/f3fb14bcc57fa2c18b9c4b72d49c4f4f.png?x-oss-process=image/quality,Q_70',
          title: '标题标题标题',
          desc: '内容内容内容'
        }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
  .item-img
    width 100%
  .item-info
    padding .1rem
    // min-width 0 为了使下方的文字...显示
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()

</style>
