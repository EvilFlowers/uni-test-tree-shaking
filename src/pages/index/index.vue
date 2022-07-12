<template>
  <view class="content">
    <image class="logo" src="../../static/logo.png"></image>
    <view>
      <text class="title">{{ title }}</text>
    </view>
    <Button type="info">主要按钮</Button>
    <Empty description="描述文字"></Empty>
    <view>{{ num }}</view>
  </view>
</template>

<script lang="ts">
import Vue from 'vue';
import {Button, Empty} from "vant";
import { add } from 'lodash'

export default Vue.extend({
  components: { Button, Empty },
  data() {
    return {
      title: 'Hello',
      num: 0,
    }
  },
  onLoad() {
    this.num = add(10, 20)
  },
  methods: {}
});
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200 rpx;
  width: 200 rpx;
  margin: 200 rpx auto 50 rpx auto;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36 rpx;
  color: #8f8f94;
}
</style>
