<template>
    <div class="swiper">
        <swiper :options="swiperOption" v-if="showSwoper">
            <!-- slides -->
            <swiper-slide v-for="item of list" :key="item.id">
                <img class="swiper-banner" :src="item.imgURL" alt="">
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 5000
      }
    }
  },
  computed: {
    showSwoper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
    .swiper >>> .swiper-pagination-bullet
        background #ffffff
    .swiper
        overflow hidden
        width :100%
        height :0
        padding-bottom :26.5%
        .swiper-banner
            width :100%;
</style>
