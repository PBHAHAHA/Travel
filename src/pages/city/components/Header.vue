<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'City'
}
</script>
<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .header
    overflow hidden
    height $headerHeight
    line-height  $headerHeight
    text-align center
    color #fff
    font-size .32rem
    background-color $bgColor
    position relative
    .header-back
      width .64rem
      text-align center
      font-size .4rem
      color #fff
      position absolute
      top 0
      left 0
</style>
