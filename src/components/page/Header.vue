<template>
  <div class="header">
      <div class="header-left">返回</div>
      <div class="header-input">输入城市景点游玩主题</div>
      <div class="header-right">城市</div>
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
.header 
    display:flex
    line-height: 3.86rem
    background:#00bcd4
    color:#fff
    .header-left
        width:2.64rem
        float:left
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
    .header-right
        width:5.24rem
        float:right
        text-align:center
</style>

