<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩/主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont city-icon">&#xe64a;</span>
    </div>
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
    height .86rem
    background  $bgColor
    line-height .86rem
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
      width 1.24rem
      float right
      text-align center
      .city-icon
        font-size .2rem
</style>
