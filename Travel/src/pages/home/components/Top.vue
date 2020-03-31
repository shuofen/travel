<template>
  <div class='top'>
    <div class='top-title'>
      <img src='http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png'/>
      <span class='top-title-txt'>本周热门榜单</span>
      <a class='top-all'>全部榜单<span class='iconfont arrow-right'>&#xe653;</span></a>
    </div>
    <ul class='top-list'>
      <li class='top-list-li' v-for='item of topList' :key='item.id'>
         <div class='top-icon' v-if='item.imgIcon'>
          <img :src='item.imgIcon'/>
        </div>
        <div class='top-img'>
          <img :src='item.imgUrl'/>
        </div>
        <div class='top-desc-text'>
          {{item.desc}}
        </div>
        <div class='price'>
          <span class='price-unit'>¥<em class='price-number'> {{item.price}}</em></span>起
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeTop',
  data () {
    return {
      topList: [{
        id: 1,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/c4/c4b6c51a2ac942cfa3.img.jpg_250x250_24fa639b.jpg',
        imgIcon: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
        desc: '花舞人间',
        price: 69.9
      }, {
        id: 2,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/1f/1f39774291457a42a3.img.jpg_250x250_f06edca8.jpg',
        imgIcon: 'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
        desc: '石象湖',
        price: 45.5
      }, {
        id: 3,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/f6/f60edcaa8934d4fda3.img.jpg_250x250_826bd8cd.jpg',
        imgIcon: 'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png',
        desc: '天府花溪谷山地户外运动体验公园',
        price: 55
      }, {
        id: 4,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/b0/b0132e78efa00572.water.jpg_250x250_419e0690.jpg',
        imgIcon: '',
        desc: '青城山',
        price: 77
      }, {
        id: 5,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201407/03/a584374ee80b738e2600d6bcaf1299e3.jpg_250x250_986e4594.jpg',
        imgIcon: '',
        desc: '都江堰',
        price: 78
      }, {
        id: 6,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/6d/6de192f67ebc1470a3.img.jpg_250x250_443bdd9c.jpg',
        imgIcon: '',
        desc: '漫花庄园',
        price: 53
      }, {
        id: 7,
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201309/24/977fea7b3c5cd758c8d65eac.jpg_250x250_145eeeb5.jpg',
        imgIcon: '',
        desc: '成都大熊猫繁育研究基地',
        price: 52
      }]
    }
  }
}
</script>
<style lang='scss' scoped>
@import '~styles/mixin.scss';
  .top{
      .top-title{
          position: relative;
          padding: .24rem 0 .26rem;
          img{
              width: .3rem;
              height: .3rem;
              margin-left: .2rem;
              vertical-align: top;
          }
          .top-title-txt{
              display: inline-block;
              height: .44rem;
              line-height: .44rem;
              font-size: .32rem;
              color: #212121;
          }
          .top-all{
              position: absolute;
              top: .36rem;
              right: .32rem;
              color: #616161;
              font-size: .24rem;
              line-height: .28rem
          }
      }
      .top-list{
          padding: 0 .24rem;
          overflow-x: scroll;
          white-space: nowrap;
          .top-list-li:not(:first-child) {
              margin-left: .12rem;
          }
          .top-list-li{
              position: relative;
              display: inline-block;
              padding: .06rem 0 .2rem;
              width: 2rem;
              .top-icon{
                  position: absolute;
                  top: 0;
                  left: 0;
                  z-index: 1;
                  overflow: hidden;
                  width: .84rem;
                  height: .4rem;
                  img {
                      width: 100%;
                  }
              }
              .top-img{
                  overflow: hidden;
                  width: 2rem;
                  height: 0;
                  padding-bottom: 100%;
                  img{
                      width: 100%;
                  }
              }
              .top-desc-text{
                      margin-top: .12rem;
                      color: #212121;
                      font-size: .24rem;
                      line-height: .32rem;
                      text-align: center;
                      width: 100%;
                      @include ellipseTxt;
              }
              .price{
                  color: #616161;
                  font-size: .24rem;
                  line-height: .36rem;
                  text-align: center;
                  .price-unit{
                    font-size: .24rem;
                    line-height: .36rem;
                    text-align: center;
                    color: #ff8300;
                  }
                  .price-number{
                    font-size: .28rem;
                  }
              }
          }
      }
  }
</style>
