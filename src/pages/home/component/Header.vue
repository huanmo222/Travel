<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/游玩/旅游景点
    </div>
    <router-link to='/city'>
      <div class="header-right">
        {{city}}
        <span class="iconfont arrow-icon">&#xe6aa;</span>
      </div>
    </router-link>

  </div>

</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
    // ...mapGetters(['doubleCity'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem /* 32/50 */
      float: left
      text-align: center
      .back-icon
        font-size: .4rem
    .header-input
      flex: 1
      line-height: .64rem /* 32/50 */
      height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background :#fff
      border-radius: .1rem /* 5/50 */
      color: #ccc
    .header-right
      min-width: 1.04rem /* 62/50 */
      padding 0 .1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -0.04rem
        font-size: .24rem
</style>
