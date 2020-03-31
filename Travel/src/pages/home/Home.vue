<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
  <home-icons></home-icons>
  <home-top></home-top>
  <home-recommend></home-recommend>
</div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeTop from './components/Top'
import HomeRecommend from './components/Recommend'
export default {
  name: 'Home',
  components: {
    HomeHeader, HomeSwiper, HomeIcons, HomeTop, HomeRecommend
  }
}
</script>
<style>
</style>
