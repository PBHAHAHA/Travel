<template>
  <div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_600x330_5d562f69.jpg" alt="">
        <div class="banner-info">
          <div class="banner-title">
            大连圣亚海洋世界
          </div>
          <div class="banner-number">
            <span class="iconfont banner-icon">&#xe6ee;</span><span>39</span>
          </div>
        </div>
    </div>
    <fade-animation>
      <common-gallary @close="handleGallaryClose" :imgs="imgs" v-show="showGallary"></common-gallary>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_350x240_9f522f2c.jpg',
        'http://img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_350x240_9f522f2c.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
  }
}
</script>
<style lang="stylus" scoped>
  .banner
    overflow hidden
    height 0
    padding-bottom 55%
    position relative
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      bottom 0
      right 0
      left 0
      line-height .6rem
      font-size .32rem
      background-image linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8))
      color #fff
      padding 0 .2rem
      .banner-title
        flex 1
      .banner-number
        height .32rem
        margin-top .14rem
        padding 0 .4rem
        font-size .24rem
        line-height .32rem
        border-radius .2rem
        background-color #ff0052
        .iconfont
          font-size .24rem
</style>
