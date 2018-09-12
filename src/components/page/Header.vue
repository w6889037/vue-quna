<template>
  <div class="header">
      <div class="header-left">
        <span class="iconfont">&#xe624;</span>
      </div>
      <div class="header-input">输入城市景点游玩主题</div>
      <div class="header-right">城市
        <span class="iconfont">&#xe62d;</span>
      </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      msg: "Home Page"
    };
  }
};
</script>

<style lang="stylus" scoped>
@import '~style/varibles.styl';
.header 
    display:flex
    line-height: 3.86rem
    background:$bgColor
    color:#fff
    .header-left
        width:2.64rem
        float:left
        text-align:center
    .header-input
        flex:1
        margin-top:0.52rem
        height:2.84rem
        margin-left:.2rem
        background :#fff
        border-radius:.3rem
        color:#ccc
        line-height:2.94rem
        height:2.94rem
        padding-left:1rem
    .header-right
        width:5.24rem
        float:right
        text-align:center
</style>

