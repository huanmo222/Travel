<template>
  <div>
    <detail-banner
      :sightName="sightName"
      :bannerImg="bannerImg"
      :gallaryImgs="gallaryImgs"
    ></detail-banner>
    <detail-header></detail-header>
    <detail-list :list="categoryList"></detail-list>
    <div class="contents"></div>
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
      sightName: '',
      gallaryImgs: [],
      categoryList: [],
      bannerImg: ''
    }
  },
  mounted () {
    this.getDetailInfo()
  },
  methods: {
    getDetailInfo () {
      this.$axios.get('/api/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.handleGetDataSucc)
    },
    handleGetDataSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.sightName = data.sightName
        this.gallaryImgs = data.gallaryImgs
        this.categoryList = data.categoryList
        this.bannerImg = data.bannerImg
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
.contents
  height 50rem

</style>
