<template>
    <view class="page-box">
        <uniStatusBar class="status"></uniStatusBar>
        <uniStatusBar></uniStatusBar>
        <view style="height:200px">滚动试试</view>
        <view class="box1" :style="{ top: statusBarHeight }">box1</view>
        <view class="box2">box2</view>
        <view style="height:200px"></view>
    </view>
</template>
 
<script>
    var statusBarHeight = uni.getSystemInfoSync().statusBarHeight + 'px';//uniapp获取手机状态栏的高度
    export default {
        data() {
            return {
                statusBarHeight: statusBarHeight
            };
        },
    }
</script>
 
<style scoped>
    .page-box{
        height: 1000px;
    }
    .status{
        position: fixed;
        top: 0;
        left: 0;
        z-index: 999;
        background: #FFFFFF;
    }
    .box1 {
      position: -webkit-sticky;
      position: sticky;
      width: 100%;
      height: 30px;
      text-align: center;
      color: #fff;
      margin-bottom: 50px;
      z-index: 1;
      background: #007bff;
    }
     
     
    .box2 {
      background: #f4516c;
      width: 100%;
      height: 30px;
      text-align: center;
    }
</style>
