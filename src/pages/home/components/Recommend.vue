<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_200x200_36727f69.jpg',
        title: '金海湖风景区',
        desc: '欢迎来景海湖风景区，这儿有你抵挡不住的诱惑,限时折扣漂亮的遭不住！！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
        title: '故宫',
        desc: '古代人类智慧，见证建筑史的历史'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_200x200_2cce447f.jpg',
        title: '颐和园',
        desc: '痛忆屈辱，居安思危。古代人类智慧，见证建筑史的历史'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '../../../assets/styles/mixins.styl'
  .title
    line-height .4rem
    background-color #ccc
    text-indent .2rem
    margin-top .2rem
  .item
    overflow hidden
    display: flex
    height: 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      min-width 0
      flex 1
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #aaa
        ellipsis()
      .item-button
        margin-top .16rem
        color #ffffff
        line-height .44rem
        background-color #ff9300
        padding 0 .1rem
        border-radius .06rem

</style>
