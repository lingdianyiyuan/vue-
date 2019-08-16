<template>
    <div class="header">
        <router-link to="/">
            <div class="header-left iconfont">&#xe601;</div>
        </router-link>
        <div class="header-center">城市选择</div>
    </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
.header
    height .86rem;
    background :$bgColor;
    .header-left
        display :inline-block;
        float :left;
        font-size: .44rem;
        color: #fff;
        line-height: .86rem;
    .header-center
        line-height :.86rem;
        color :#fff;
        text-align :center;
</style>
