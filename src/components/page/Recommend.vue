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
    data (){
        return {
            recommendList:[{
                id:"01",
                imgUrl:"https://youimg1.c-ctrip.com/target/10090r000000hffxs7E31_D_228_170_Mtg_7.jpg",
                text1:"上海迪士尼旅游度假区",
                text2:"5星级景区",
                text3:"9.6万条评价",
                text4:"查看详情"
            },{
                id:"02",
                imgUrl:"https://youimg1.c-ctrip.com/target/10090r000000hffxs7E31_D_228_170_Mtg_7.jpg",
                text1:"大连圣亚海洋世界旅游度假区",
                text2:"5星级景区",
                text3:"9.7万条评价",
                text4:"查看详情"
            },{
                id:"03",
                imgUrl:"https://youimg1.c-ctrip.com/target/10090r000000hffxs7E31_D_228_170_Mtg_7.jpg",
                text1:"湖南张家界旅游度假区",
                text2:"5星级景区",
                text3:"9.5万条评价",
                text4:"查看详情"
            }]
        }
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
