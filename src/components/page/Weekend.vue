<template>
    <div class="weekend">
        <div class="weekend-title">周末去哪</div>
        <div class="weekend-content" v-for="item of weekList" :key="item.id">
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
    data(){
        return {
            weekList:[{
                id:"01",
                imgUrl:"https://pics.lvjs.com.cn/pics//uploads/pc/place2/2016-03-04/be95a9bb-3454-448d-8a00-29a24a35b24f.jpg",
                desc:"华东五市、双水乡双高5日跟团游(两成人立减100，接送1条龙  舒适酒店 赠送三大游船体验 太湖鼋头渚 古镇乌篷摇橹船 船游太湖赏荷花 西湖游船赏十景)"
            },{
                id:"02",
                imgUrl:"https://pics.lvjs.com.cn/pics//uploads/pc/place2/2018-07-18/a99e7833-1053-4417-9e6d-744a3a41312f.jpg",
                desc:"华东五市、双水乡双高5日跟团游(两成人立减100，接送1条龙  舒适酒店 赠送三大游船体验 太湖鼋头渚 古镇乌篷摇橹船 船游太湖赏荷花 西湖游船赏十景)"
            },{
                id:"03",
                imgUrl:"https://pics.lvjs.com.cn/pics//uploads/pc/place2/2016-03-04/be95a9bb-3454-448d-8a00-29a24a35b24f.jpg",
                desc:"华东五市、双水乡双高5日跟团游(两成人立减100，接送1条龙  舒适酒店 赠送三大游船体验 太湖鼋头渚 古镇乌篷摇橹船 船游太湖赏荷花 西湖游船赏十景)"
            }]
        }
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

