<template>
<div class="header">
    <div class="header-left">
        <div class="iconfont back-icon">&#xe601;</div>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe65c;</span>
        输入城市/景点/游玩主题</div>
    <router-link to="./City" >
        <div class="header-right">{{this.$store.state.city}}<span class="iconfont icon-city">&#xe600;</span></div>
    </router-link>
</div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>
<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        display :flex;
        height:.86rem;
        line-height :.86rem;
        background :$bgColor;
        color :#fff;
        .header-left
            width:.64rem;
            float:left;
            .back-icon
                text-align :center;
                font-size :.4rem;
        .header-input
            flex :1;
            height:.64rem;
            margin-top:.12rem;
            margin-left:.2rem;
            line-height:.64rem;
            border-radius:.1rem;
            background :#fff;
            color :#ccc;
            padding-left :.24rem;
        .header-right
            width :1.24rem;
            float :right;
            text-align :center;
            color :#fff;
            .icon-city
                margin-left :.04rem;
</style>
