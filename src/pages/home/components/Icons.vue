<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="https://qcommons.qunar.com/headshot/headshotsById/239042366.png?s&ssl=true" alt="">
      </div>
      <p class="icon-desc">热门景点</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  @import "~style/varibles.styl";
  .icons{ overflow hidden; height:0; padding-bottom:50%;}
  .icon{height:0;position relative;overflow hidden;float:left;width:25%;padding-bottom:25%;}
  .icon-img{ position absolute;top:0;left:0;right:0;bottom:.44rem;box-sizing:border-box;padding .44rem;}
  .icon-img-content{display block;margin:0 auto;height:180%}
  .icon-desc{position absolute;line-height .44rem;text-align center;height .44rem;left:0;right:0;bottom:0;color:$darkTextColor}
</style>
