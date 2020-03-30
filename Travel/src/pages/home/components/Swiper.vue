<template>
    <div class='swiper'>
        <swiper ref="mySwiper" :options="swiperOptions">
            <swiper-slide v-for="banner of bannerList" :key="banner.id">
              <img class='banner-img' :src="banner.imgUrl" />
            </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    </div>
</template>
<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
export default {
  name: 'HomeSwiper',
  components: {
    swiper, swiperSlide
  },
  data () {
    return {
      swiperOptions: {
        loop: true,
        pagination: '.swiper-pagination'
      },
      bannerList: [{
        id: 1,
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg'
      }, {
        id: 2,
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg'
      }]
    }
  }
}
</script>
<style lang='scss' scoped>
.swiper >>> .swiper-pagination-bullet-active{
    background:#fff;
}
.banner-img{
    width:100%;
}
</style>
