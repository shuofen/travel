<template>
  <div class='icons'>
    <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
     <div class='icon'>
      <div class='icon-img'>
        <img class='icon-img-content' src='http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png' />
      </div>
      <p class='icon-desc'>景点门票</p>
    </div>
    <div class='test'></div>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons'
}
</script>
<style lang='scss' scoped>
  .icons {
    .test {
        height: .2rem;
    }
    height: 0;
    width: 100%;
    overflow: hidden;
    padding-bottom: 50%;
    .icon {
      position: relative;
      height: 0;
      width: 25%;
      float: left;
      padding-bottom: 21.5%;
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
      height: .44rem;
      line-height: .44rem;
      text-align: center;
      color: #333;
    }
  }
</style>
