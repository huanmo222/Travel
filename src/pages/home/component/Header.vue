<template>
  <div class="header">
    <div class="header-left">返回</div>
    <div class="header-input">输入城市</div>
    <div class="header-right">1</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    line-height: .86rem
    background: #00bcd4
    color: #fff
    .header-left
      width: .64rem /* 32/50 */
      float: left
      text-align: center
    .header-input
      flex: 1
      line-height: .64rem /* 32/50 */
      height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      background :#fff
      border-radius: .1rem /* 5/50 */
      color: #ccc
    .header-right
      width: 1.24rem /* 62/50 */
      float: right
      text-align: center
</style>
