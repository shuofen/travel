<template>
  <div class='icons'>
   <swiper :options="swiperOptions">
            <swiper-slide v-for='(page, index) of pages' :key='index'>
              <div class='icon'  v-for='icon of page' :key='icon.id'>
                <div class='icon-img'>
                  <img class='icon-img-content' :src='icon.imgUrl'/>
                </div>
                <p class='icon-desc'>{{icon.desc}}</p>
              </div>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination" v-if = 'pages.length>1'></div>
    </swiper>
  </div>
</template>
<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
export default {
  name: 'HomeIcons',
  components: {
    swiper, swiperSlide
  },
  data () {
    return {
      swiperOptions: {
        loop: true,
        pagination: '.swiper-pagination'
      },
      iconsList: [{
        id: 1,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 2,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/c1/6f15f887179fa002.png',
        desc: '颐和园'
      }, {
        id: 3,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/4c/eac47dd8def8de02.png',
        desc: '北京世博园'
      }, {
        id: 4,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        desc: '玉渊潭公园'
      }, {
        id: 5,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      }, {
        id: 6,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
        desc: '古北水镇'
      }, {
        id: 7,
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '向上公园'
      }, {
        id: 8,
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '凤凰岭'
      }, {
        id: 9,
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '凤凰岭'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang='scss' scoped>
@import '~styles/varible.scss';
@import '~styles/mixin.scss';
 .icons >>> .swiper-pagination-bullet-active{
      background: rgba(0,175,190,.8);
  }
  .icons >>> .swiper-container{
    height: 0;
    width: 100%;
    padding-bottom: 50%;
  }
  .icons {
    .test {
        height: .2rem;
    }
    .icon {
      position: relative;
      height: 0;
      width: 25%;
      float: left;
      padding-bottom: 1.5rem;
      overflow: hidden;
      text-align: center;
    }
    .icon-img {
      position: absolute;
      top: .1rem;
      left: 0;
      right: 0;
      bottom: .44rem;
      .icon-img-content {
        width: 1.1rem;
        height: 1.1rem;
      }
    }
    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      text-align: center;
      color: $darkTxtColor;
      @include ellipseTxt;
    }
  }
</style>
