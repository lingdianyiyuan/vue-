<template>
    <div class="weekend">
        <div class="weekend-title">
            周末去哪儿
        </div>
        <div class="weekend-content border-bottom">
            <ul>
                <li v-for="item of week" :key="item.id">
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
  props: {
    week: Array
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
