<template>
    <div class="weekend">
        <div class="weekend-title">
            周末去哪儿
        </div>
        <div class="weekend-content border-bottom">
            <ul>
                <li v-for="item of WeekendList" :key="item.id">
                    <img class="weekend-content-img" :src="item.imgURL" alt="">
                    <p class="weekend-add">{{item.add}}</p>
                    <p class="weekend-description">{{item.description}}</p>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      WeekendList: [
        {
          id: '001',
          imgURL: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
          add: '京城周末撒欢',
          description: '在帝都过周末，不仅仅是城中游'
        },
        {
          id: '002',
          imgURL: 'http://img1.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg',
          add: '京城溜娃必去',
          description: '德智体美劳全面发展的亲子日，这些地方该去看看…'
        },
        {
          id: '003',
          imgURL: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
          add: '帝都必打卡',
          description: '来北京必去的景点非这些地方莫属'
        },
        {
          id: '004',
          imgURL: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
          add: '漂流勇进，烧烤露营',
          description: '轻松水上漂，任我乐逍遥'
        },
        {
          id: '005',
          imgURL: 'http://img1.qunarzz.com/sight/source/1505/53/02091f1ee43d0a.jpg_r_640x214_2e3256b1.jpg',
          add: '北京清凉避暑胜地',
          description: '到大自然中享受“天然空调”的清凉'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/minins.styl';
    .weekend
        margin-top :.1rem;
        .weekend-title
            height :.8rem;
            line-height :.8rem;
            background :#eee;
            padding-left :.26rem;
        .weekend-content
            height :4rem;
            padding-bottom :.2rem;
            .weekend-content-img
                width :100%;
                height :3rem;
            .weekend-add
                font-size :.28rem;
                line-height :.44rem;
                padding :.2rem 1.4rem 0 .2rem;
                ellipsis()
            .weekend-description
                font-size :.24rem;
                line-height :.44rem;
                padding-right :1.4rem;
                padding-left :.2rem;
                color #616161;
                ellipsis()
</style>
