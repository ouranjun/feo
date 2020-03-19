<template>
  <div>
      <swiper :options="swiperOptions">
    <swiper-slide v-for="(item, index) in bannerImg" :key="index">
      <a :href="item.linkUrl">
        <img class="bannerImg" :src="item.picUrl" alt="">
      </a>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
export default {
  data () {
    return {
      bannerImg: [
        {
          linkUrl: 'https://item.rakuten.co.jp/fedonline/hl701/',
          picUrl: require('@/assets/img/ban-701.jpg')
        },
        {
          linkUrl: 'https://item.rakuten.co.jp/fedonline/c/0000000131/',
          picUrl: require('@/assets/img/400-5.jpg')
        },
        {
          linkUrl: 'https://item.rakuten.co.jp/fedonline/hl901/',
          picUrl: require('@/assets/img/banner-901.jpg')
        },
        {
          linkUrl: 'https://www.rakuten.ne.jp/gold/fedonline/mqmsystem/sale/sale.html',
          picUrl: require('@/assets/img/xin-bann.jpg')
        }
      ],
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        },
        autoplay: {
          delay: 3000,
          stopOnLastSlide: false,
          disableOnInteraction: true
        },
        loop: true,
        height: 500
      }
    }
  },
  components: {
    Swiper,
    SwiperSlide
  },
  directives: {
    swiper: directive
  },
  created () {
    console.log(this.bannerImg[1].picUrl)
  }
}
</script>

<style scoped>
.bannerImg {
  width: 100%;
  height: 100%;
  max-width: 100%;
  min-width: 200px;
}
</style>
