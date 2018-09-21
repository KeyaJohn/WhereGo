<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">
        &#xe624;
      </div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe611;</span>
       输入城市/经典/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont">
        &#xe68f;
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  @import "~styles/varibles.style"
  .header
    display: flex
    line-height: .86rem
    background: $bgcolor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .1.3rem
      padding-left: .2rem
      background: #fff
      color: #999
      border-radius: .1rem
    .header-right
      width: 1.04rem
      float: right
      text-align: center
</style>
