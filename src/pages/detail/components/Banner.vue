<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" alt="">
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe626;</span>{{this.gallaryImgs.length}}</div>
      </div>
    </div>
    <fade-animation>
      <common-gallary :imgs="gallaryImgs" v-show="showGallary" @close="handleGallaryClick"></common-gallary>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClick () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner{overflow: hidden;height:0;padding-bottom:55%;position: relative  }
  .banner-img{width: 100%}
  .banner-info{ background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8));color:#fff;display:flex;position:absolute;left: 0;right: 0;bottom: 0;line-height: .6rem}
  .banner-title{flex:1;font-size: .32rem;padding: 0 .2rem}
  .banner-number{height: .32rem;line-height: .32rem;margin-top:.14rem;font-size:.24rem;padding: 0 .4rem;border-radius: .2rem;background: rgba(0,0,0,.8)}
  .banner-icon{font-size: .24rem}
</style>
