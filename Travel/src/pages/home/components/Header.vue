<template>
<div class='header'>
    <div class='header-left'>
        <div class='iconfont back-icon'>&#xe624;</div>
    </div>
    <div class='header-input'>
        <span class='iconfont'>&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
    <div class='header-right'>
        城市
        <span class='iconfont arrow-icon'>&#xe771;</span>
    </div>
</div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>
<style lang='scss' scoped>
    @import '~styles/varible.scss';
    .header{
        display:flex;
        height:.86rem;
        line-height:.86rem;
        color:#fff;
        background:$bgColor;
        .header-left{
            float:left;
            width:.64rem;
            .back-icon{
                text-align:center;
            }
        }
        .header-input{
            margin-top:.12rem;
            height:.64rem;
            margin-left:.2rem;
            float:left;
            flex:1;
            padding-left:.2rem;
            background:#fff;
            border-radius:.1rem;
            color:#ccc;
            line-height:.64rem;

        }
        .header-right{
            float:right;
            text-align:center;
            width:1.24rem;
            .arrow-icon{
                font-size:.24rem;
                margin-left:-.04rem;
            }
        }
    }
</style>
