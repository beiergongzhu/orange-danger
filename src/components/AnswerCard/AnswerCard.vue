<template>
  <view class="content">
    <view class="top">
      <view class="user">woiehfoie</view>
      <view class="time">2022-1-16</view>
    </view>
    <view class="answer">
      你好，叶片干枯引发的原因多样，一般多见于肥害或根系问题或气候骤变引发生理问题。可根据当时的情况酌情判断。
    </view>
  </view>
</template>

<script lang='ts'>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'AnswerCard',
  setup() {

  },
})
</script>

<style lang="scss" scoped>
.content {
  background-color: #fff;
  width: 90vw;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 20px;
  margin-bottom: 20px;

  .top {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;

    .user {
      font-size: 16px;
    }

    .time {
      color: #bbbcbc;
      font-size: 14px;
    }
  }

  .answer {}
}
</style>