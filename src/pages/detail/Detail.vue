<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-list :list="list"></detail-list>
  </div>
</template>

<script>
import DetailBanner from './component/Banner'
import DetailHeader from './component/Header'
import DetailList from './component/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '成人票',
        children: [{
          title: '成人三馆联票1',
          children: [{
            title: '成人三馆联票1-1'
          }, {
            title: '成人三馆联票1-2'
          }]
        }, {
          title: '成人三馆联票2'
        }]
      }, {
        title: '学生票'
      }, {
        title: '儿童票'
      }, {
        title: '特惠票'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>
