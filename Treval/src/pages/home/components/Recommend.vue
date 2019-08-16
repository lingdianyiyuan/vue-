<template>
  <div class='recommend-content'>
    <div class='recommend-title'>
      <img
        class='recommend-img'
        src='http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png'
        alt
      />
      本周热门榜单
      <div class='popularList'>
        全部榜单
        <span class='iconfont'>&#xe612;</span>
      </div>
    </div>
    <div class='recommend-list'>
      <swiper :options='swiperOption'>
        <!-- slides -->
        <swiper-slide v-for='item of commend' :key='item.id'>
          <img class='popularList-img' :src='item.imgURL' alt />
          <p class='popularList-title'>{{item.title}}</p>
          <p class='popularList-price'><span class="priceColor">￥{{item.price}}</span>起</p>
        </swiper-slide>
        <!-- Optional controls -->
        <!-- <div class='swiper-pagination' slot='pagination'></div> -->
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    commend: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiperOption',
        cssWidthAndHeight: false,
        slidesPerView: 3.7,
        offsetSlidesAfter: 2,
        centeredSlides: false
      }
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/minins.styl'
.recommend-content >>> .swiper-slide
    width :2rem !important;
    margin :.1rem;
.recommend-content
    margin-top: 0.2rem;
    background :#ffffff;
    .recommend-title
        height: 0.44rem;
        padding: .1rem 0.1rem;
        line-height: 0.44rem;
        font-size: 0.32rem;
        .recommend-img
            width: 0.3rem;
            height: 0.3rem;
            vertical-align: top;
            margin-left: 0.2rem;
        .popularList
            float :right;
    .popularList-img
        width :2rem;
        height :2rem;
        margin-left :.1rem;
    .popularList-title
        box-sizing :border-box;
        padding :.15rem 0;
        text-align :center;
        color :#212121;
        ellipsis()
    .popularList-price
        box-sizing :border-box;
        text-align :center;
        color :#212121;
        .priceColor
          color :#ff8300;
</style>
