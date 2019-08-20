<template>
    <div class="search">
        <input type="text" class="search-input" placeholder="根据城市或拼音搜索">
    </div>
</template>

<script>
export default {
  name: 'CitySearch.vue'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
    .search
        height :.7rem;
        padding :0 .1rem;
        background :$bgColor;
        .search-input
            width :100%;
            height :.62rem;
            line-height :.62rem;
            box-sizing :border-box;
            padding :0 .1rem;
            border-radius :.06rem;
            text-align :center;
            color :#666;
</style>
