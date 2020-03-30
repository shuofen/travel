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
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20203/964508ac574bc7e85d5c17bb1e9dd65c.jpg_750x200_293b242d.jpg'
      }, {
        id: 2,
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20203/964508ac574bc7e85d5c17bb1e9dd65c.jpg_750x200_293b242d.jpg'
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
