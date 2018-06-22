<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import "~style/varibles.styl";
  .header{ line-height:$headerHeight;display: flex;background:$bgColor;color: white }

  .header-left{ width:.64rem;float:left }
  .back-icon{text-align: center;font-size:.4rem}

  .header-input{padding-left:.2rem;color:#ccc;flex:1;height:.64rem;line-height:.64rem;margin-left:.2rem;margin-top: .12rem;background:#fff;border-radius: .1rem}

  .header-right{color: #fff; width: 1.24rem;float: right;text-align: center }
  .arrow-icon{font-size: .24rem;margin-left: -.04rem}
</style>
