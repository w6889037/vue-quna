<template>
    <div class="recommend">
        <div class="recommend-title">热销推荐</div>
        <div class="recommend-content" v-for="item of recommendList" :key="item.id">
            <div class="recommend-content-img">
                <img :src="item.imgUrl">
            </div>
            <div class="recommend-content-text">
                <div class="text1">{{item.text1}}</div>
                <div class="text2">{{item.text2}}</div>
                <div class="text3">{{item.text3}}</div>
                <div class="text4"><button>{{item.text4}}</button></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"HomeRecommend",
    props: {
        recommendList: Array
    }
}
</script>

<style lang="stylus" scoped>
    .recommend-title
        background:#eee
        padding:0.5rem
    .recommend-content
        display:flex
        flex-direction:row
        padding:0.5rem
        .recommend-content-img
            width:6.875rem
            height:100%
        .recommend-content-img > img 
            width:6.875rem
            height:100%
        .recommend-content-text
            flex:1
            padding-left:0.5rem
            .text1
                font-size:1.0625rem
                font-family: 'PingFangSC-Regular'
            .text2,.text3
                font-size:.75rem
                font-family: 'PingFangSC-Regular'
                color: #666666
                padding-bottom:0rem /* 0/16 */
</style>
