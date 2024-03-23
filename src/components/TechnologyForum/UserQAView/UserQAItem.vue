<template>
  <view class="content" @click="navigateToDetail">
    <view class="top">
      <view class="user">
        jingqiang
      </view>
      <view class="time">2021-11-06</view>
    </view>
    <view class="title">
      请问专家，现在11月6号了，沃柑还可以喷青苔吗
    </view>
    <view class="bottom">
      <view class="star">
        <img src="@/static/MyCollection/collection-on.png" alt="star">
        <span>收藏 1</span>
      </view>
      <view class="answer">
        <img src="@/static/answer_num.png" alt="">
        <span>回答 0</span>
      </view>
    </view>
  </view>
</template>

<script lang='ts'>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'UserQAItem',
  setup() {
    // 跳转问题详情
    const navigateToDetail = () => {
      uni.navigateTo({
        url: `/pages/QADetail/QADetail`,
      })
    }

    return { navigateToDetail }
  },
})
</script>

<style lang="scss" scoped>
.content {
  width: 90vw;
  height: 170px;
  background-color: #fff;
  border-radius: 20px;
  margin-bottom: 4vh;
  padding: 20px;
  box-sizing: border-box;
  box-shadow: 8px 8px 5px lightgray;

  .top {
    display: flex;
    justify-content: space-between;

    .user {
      font-size: 14px;
    }

    .time {
      color: #bbbcbc;
      font-size: 12px;
    }
  }

  .title {
    margin-top: 20px;
    height: 60px;
    font-size: 18px;
  }

  .bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 40px;

    .star {
      width: 80px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: space-around;

      img {
        width: 20px;
        height: 20px;
      }

      span {
        font-size: 14px;
        color: #ffa500;
      }
    }

    .answer {
      display: flex;
      align-items: center;
      height: 40px;
      width: 80px;
      justify-content: space-around;

      img {
        width: 20px;
        height: 20px;
        margin-top: 2px;
      }

      span {
        font-size: 14px;
        color: #bbbcbc;
      }
    }
  }
}
</style>