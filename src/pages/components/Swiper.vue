<template>
  <div>
    <swiper :options="swiperOption">
      <swiper-slide v-for="(slide, index) in swiperSlides" :key="index">
        <img class="swiper-img" v-bind:src="slide"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'scarrousel',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 4000, //  可选选项，自动滑动
        autoplayDisableOnInteraction: false // 注意此参数，默认为true
      },
      swiperSlides: ['https://img1.qunarzz.com/vc/f3/ea/ae/095dd61c09f2797ba9147bd03f.jpg', 'https://img1.qunarzz.com/vc/4e/c2/9a/61222b895136533c133ee9e8bc.jpg', 'https://img1.qunarzz.com/vc/1f/ba/ac/13c3552a1cb338991301f9b0ad.jpg', 'https://img1.qunarzz.com/vc/ce/4b/45/7f78e2003fb5fb65c57eb1a800.jpg']
    }
  },
  mounted () {
    setInterval(() => {
      console.log('simulate async data')
      if (this.swiperSlides.length < 4) {
        this.swiperSlides.push(this.swiperSlides.length + 1)
      }
    }, 3000)
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: red
  .swiper-img
    width: 100%
</style>
