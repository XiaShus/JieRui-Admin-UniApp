<template>
  <view class="content">

    <!-- 顶部搜索 -->
    <view class="">
      <u-search :showAction="true" actionText="搜索" :animation="false"></u-search>
    </view>
    <!-- 快捷功能区 -->
    <view class="">
      <view>
        <u-icon name="photo" color="#2979ff" size="100"></u-icon>
        <text></text>
      </view>
      <view>
        <u-icon name="photo"></u-icon>
      </view>
      <view>
        <u-icon name="photo"></u-icon>
      </view>
      <view>
        <u-icon name="photo"></u-icon>
      </view>
    </view>
    <!-- 常用功能区 -->
    <view class="">

    </view>
    <!-- 滚动公告 -->
    <view class="">
      <view class="notice-box">

      </view>
    </view>
    <!-- 混合功能区 -->
    <view class="">

    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      keyword: '遥看瀑布挂前川'
    }
  },
  onLoad: function () {
  }
}
</script>

<style>
.content {
  padding: 20px;
}

.notice-box {
  background-color: #1cbbb4;
}
</style>
