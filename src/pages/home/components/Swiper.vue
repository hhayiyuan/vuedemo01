<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgURL">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgURL: '//ad.qunarzz.com/ad/picture/93cec2ff-bf9d-4b86-8e19-7e8a45e51d71_%E5%9B%BD%E9%99%85%E8%88%AA%E7%BA%BF%E4%BD%8E%E4%BB%B7%E4%BF%83%E9%94%80%203W%E5%9B%BE.jpg'
      }, {
        id: '0002',
        imgURL: '//ad.qunarzz.com/ad/picture/bb0b03d9-0eae-49ec-92e2-4345bac8ad9a_3w-%E6%9C%BA%E7%A5%A8%E9%A6%96%E9%A1%B5--912-170--.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper>>>.swiper-pagination-bullet-active{background: #fff!important;}
  .wrapper{background:#eee;width: 100%;height: 0;overflow: hidden;padding-bottom:18.6% }
  .swiper-img{width: 100%}
</style>
