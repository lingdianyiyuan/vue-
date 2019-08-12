<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index ) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgURL" alt/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      IconsList: [
        {
          id: '001',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '景点门票'
        },
        {
          id: '002',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          desc: '故宫'
        },
        {
          id: '003',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc: '北京必游'
        },
        {
          id: '004',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
          desc: '水上乐园'
        },
        {
          id: '005',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
          desc: '一日游'
        },
        {
          id: '006',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
          desc: '古北水镇'
        },
        {
          id: '007',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desc: '动植物园'
        },
        {
          id: '008',
          imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
          desc: '北京野生动物园'
        },
        {
          id: '009',
          imgURL: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b4511345827006994aa1980a3886f0ac.png',
          desc: '北京世园会'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.IconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/minins.styl'
@import '~styles/varibles.styl'
.icons >>> .swiper-container
  height: 0;
  padding-bottom: 50%;
.icon
    float: left;
    position: relative;
    overflow: hidden;
    width: 25%;
    height: 0;
    padding-bottom: 25%;

    .icon-img
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding: 0.1rem;
      .icon-img-content
        display: block;
        margin: 0 auto;
        height: 100%;
    .icon-desc
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      text-align: center;
      color: $textColor;
      ellipsis()
</style>
