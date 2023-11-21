<template>
  <view class="content">

    <!-- 顶部搜索 -->
    <view class="">
      <u-row>
        <u-col :span="11">
          <u-search
              v-model="keyword"
              :show-action="false"
              @change="change"
          ></u-search>
        </u-col>
        <u-col span="1" >
          <u-icon name="bell" color="#FFFFFF" size="30"></u-icon>
        </u-col>
      </u-row>

    </view>
    <!-- 快捷功能区 -->
    <view class="core-func-box">
      <u-row justify="center" customStyle="margin-bottom: 10px">
        <u-col align="center" span="3" v-for="v in coreFunction">
          <view style="text-align: center">
            <u-icon :name="v.icon" color="#FFFFFF" size="100"></u-icon>
            <text>{{ v.title }}</text>
          </view>
        </u-col>
      </u-row>
    </view>
    <!-- 常用功能区 -->
    <view class="common-func-box">
      <u-row style="flex-wrap: wrap" customStyle="margin-bottom: 10px">
        <u-col span="2.4" v-for="v in commonFunction">
          <view style="text-align: center">
            <u-icon :name="v.icon" color="#00000" size="50"></u-icon>
            <text>{{ v.title }}</text>
          </view>
        </u-col>
      </u-row>
    </view>
    <!-- 滚动公告 -->
    <view class="notice-box">

    </view>
    <!-- 混合功能区 -->
    <view class="">

    </view>
  </view>
</template>

<script>
import UniCard from "../uni_modules/uni-card/components/uni-card/uni-card.vue";

export default {
  components: {UniCard},
  data() {
    return {
      keyword: '',
      coreFunction: [
        {
          icon: 'photo',
          title: '123',
          path: ''
        },
        {
          icon: 'scan',
          title: '扫一扫',
          path: ''
        },
        {
          icon: 'photo',
          title: '123',
          path: ''
        },
        {
          icon: 'photo',
          title: '123',
          path: ''
        },
      ],
      commonFunction: [
        {
          icon: 'photo',
          title: '质量管理',
          path: ''
        },
        {
          icon: 'photo',
          title: '安全管理',
          path: ''
        },
        {
          icon: 'photo',
          title: '网盘管理',
          path: ''
        },
        {
          icon: 'photo',
          title: '任务中心',
          path: ''
        },
        {
          icon: 'photo',
          title: '数据中心',
          path: ''
        },
      ],
      noticeData: [],

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
  border-radius: 20px;
  width: 100%;
  height: 20px;
}

.core-func-box {
  color: #FFFFFF;
}

.common-func-box {
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 20px;
  width: 100%;
  background-color: #FFFFFF;
  color: #000000;
  flex-warp: warp;
}
</style>
