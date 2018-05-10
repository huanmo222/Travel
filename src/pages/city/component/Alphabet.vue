<template>
  <ul class="alphabet">
    <li class="item">A</li>
    <li class="item">B</li>
    <li class="item">C</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .alphabet
    display flex
    flex-direction column
    justify-content center
    position absolute
    right 0
    top 1.68rem
    bottom 0
    width .4rem
    .item
      line-height .4rem
      text-align center
      color $bgColor

</style>
