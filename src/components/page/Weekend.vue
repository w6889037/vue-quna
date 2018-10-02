<template>
    <div class="weekend">
        <div class="weekend-title">周末去哪</div>
        <div class="weekend-content" v-for="item of weekendList" :key="item.id">
            <img :src="item.imgUrl">
            <div>
                <p>{{item.desc}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"HomeWeedend",
    props: {
        weekendList: Array
    }
}
</script>

<style lang="stylus" scoped>
    .weekend-content > div
        padding:0.5rem
    .weekend-title
        background:#eee
        padding:0.5rem
    .weekend-content > img
        width:100%
        height:12rem
    .weekend-content >div > p 
        color:#000
        display:-webkit-box
        -webkit-box-orient:vertical
        -webkit-line-clamp:2
        overflow:hidden
        font-family: microsoft yahei,Arial
        font-size:.85rem
</style>

