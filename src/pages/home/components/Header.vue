<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩/主题
    </div>
      <router-link to="/city">
      <div class="header-right">
        {{this.$store.state.city}}
        <span class="iconfont city-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .header
    display flex
    height $headerHeight
    background  $bgColor
    line-height $headerHeight
    color #fff
    .header-left
      width .64rem
      float left
      .back-icon
        display block
        text-align center
        font-size .4rem
    .header-input
      flex 1
      height .64rem
      line-height .64rem
      color #ccc
      background-color #fff
      border-radius:.1rem
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
    .header-right
      min-width 1.04rem
      padding 0 .1rem
      float right
      text-align center
      color #fff
      .city-icon
        font-size .2rem
</style>
