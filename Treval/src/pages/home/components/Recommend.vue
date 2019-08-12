<template>
  <div class="recommend-content">
    <div class="recommend-title">
      <img
        class="recommend-img"
        src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png"
        alt
      />
      本周热门榜单
      <div class="popularList">
        全部榜单
        <span class="iconfont">&#xe612;</span>
      </div>
    </div>
    <div class="recommend-list">
      <swiper :options="swiperOption-recommend">
        <!-- slides -->
        <swiper-slide v-for="item of RecommendList" :key="item.id">
          <img class="popularList-img" :src="item.imgURL" alt />
          <p class="popularList-title">{{item.title}}</p>
          <p class="popularList-price">{{item.price}}</p>
        </swiper-slide>
        <!-- Optional controls -->
        <!-- <div class="swiper-pagination" slot="pagination"></div> -->
      </swiper>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data() {
    return {
    swiperOption: {
        pagination: '.swiperOption-recommend',
        slidesPerView : 3,
        centeredSlides : true,
      },
      RecommendList: [
        {
          id: "001",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg",
          title: "故宫",
          price: "￥60"
        },
        {
          id: "002",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_250x250_50c99cf3.jpg",
          title: "八达岭长城",
          price: "￥40"
        },
        {
          id: "003",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1505/f5/f5f45e1a83537bcb.water.jpg_250x250_63e3520a.jpg",
          title: "圆明园",
          price: "￥25"
        },
        {
          id: "004",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_250x250_d852635b.jpg",
          title: "颐和园",
          price: "￥38"
        },
        {
          id: "005",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/201405/12/51b63883c25f5d87af3c08bb016e2bd7.jpg_250x250_6ec2f798.jpg",
          title: "恭王府",
          price: "￥27"
        },
        {
          id: "006",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_250x250_3588bc9a.jpg",
          title: "北京世界园艺博览会",
          price: "￥108"
        },
        {
          id: "007",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_250x250_ecfa0df2.jpg",
          title: "水立方",
          price: "￥246"
        },
        {
          id: "008",
          imgURL:
            "http://img1.qunarzz.com/sight/p0/1602/92/920e47352552c1c990.water.jpg_250x250_ee99c18e.jpg",
          title: "天坛公园",
          price: "￥40"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.recommend-content >>> .swiper-slide
    width :2rem !important;
    margin :.1rem;
.recommend-content 
    margin-top: 0.2rem;
    .recommend-title 
        height: 0.44rem;
        padding: 0 0.1rem;
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
    .popularList-price
        box-sizing :border-box;
        padding :.15rem 0;
        text-align :center;

        
  

</style>
