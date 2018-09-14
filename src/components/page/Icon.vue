<template>
    <div class="wrapper">
        <swiper :options="iconOption">
            <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icons">
                    <div class="icon" v-for="item of page" :key="item.id">
                        <img class="icon-image" :src="item.imgUrl" alt="">
                        <div>
                            <p class="icon-p">{{item.desc}}</p>                    
                        </div>
                    </div>
                </div>
            </swiper-slide>
            <div class="icon-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "iconSwiper",
    data() {
        return {
            iconOption: {
                pagination: '.icon-pagination',
                loop: true
            },
            iconList: [{
                id:"01",
                imgUrl:"https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png",
                desc:"景点"
            },{
                id:"02",
                imgUrl:"https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png",
                desc:"旅游"
            },{
                id:"03",
                imgUrl:"https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png",
                desc:"景点"
            },{
                id:"04",
                imgUrl:"https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png",
                desc:"旅游"
            },{
                id:"05",
                imgUrl:"https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png",
                desc:"景点"
            },{
                id:"06",
                imgUrl:"https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png",
                desc:"旅游"
            },{
                id:"07",
                imgUrl:"https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png",
                desc:"景点"
            },{
                id:"08",
                imgUrl:"https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png",
                desc:"旅游"
            },{
                id:"09",
                imgUrl:"https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png",
                desc:"景点"
            },{
                id:"10",
                imgUrl:"https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png",
                desc:"旅游"
            },{
                id:"11",
                imgUrl:"https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png",
                desc:"景点"
            },{
                id:"12",
                imgUrl:"https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png",
                desc:"旅游"
            }]
        }
    },
    computed: {
        pages (){
            const pages=[]
            this.iconList.forEach((item,index) => {
                const page = Math.floor(index/10)
                console.log(page)
                if(!pages[page]){
                    pages[page]=[]
                }
                pages[page].push(item)
            })
            console.log(pages)
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .icons
        display:flex
        height:100%
        flex-wrap:wrap
        .icon
            width: 20%
            height: 100%
            text-align:center
            .icon-image
                width:4rem
                height:3rem
            .icon-p
                text-align:center
                font-family: Hiragino Sans GB, Arial,Helvetica, "宋体", sans-serif
                font-size:.875rem /* 14/16 */
    .icon-pagination
        text-align:center     
</style>


