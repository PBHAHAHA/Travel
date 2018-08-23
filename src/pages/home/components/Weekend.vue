<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
        title: '金海湖风景区',
        desc: '欢迎来景海湖风景区，这儿有你抵挡不住的诱惑,限时折扣漂亮的遭不住！！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/53/02091f1ee43d0a.jpg_r_640x214_2e3256b1.jpg',
        title: '故宫',
        desc: '古代人类智慧，见证建筑史的历史'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
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
    .item-img-wrapper
      overflow hidden
      height 0
      padding-bottom 33.9%
      .item-img
        width 100%
    .item-info
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #aaa
        ellipsis()
</style>
