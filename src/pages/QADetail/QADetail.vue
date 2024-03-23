<template>
  <view class="content">
    <view class="question">
      <view class="top">
        <view class="user">jingqiang</view>
        <view class="time">2021-11-06</view>
      </view>
      <view class="title">请问专家，现在11月6号了，沃柑还可以喷青苔吗</view>
    </view>
    <view class="answer">
      <view class="answer-title">回答 2</view>
      <view class="answer-list">
        <AnswerCard />
        <AnswerCard />
        <AnswerCard />
        <AnswerCard />
        <AnswerCard />
        <AnswerCard />
      </view>
    </view>
    <view class="bottom">
      <view class="star">
        <img src="@/static/MyCollection/collection-on.png" alt="star">
        <span>收藏</span>
      </view>
      <view class="answer-btn">我来回答</view>
    </view>
  </view>
</template>

<script lang='ts'>
import { defineComponent } from 'vue'
import AnswerCard from '@/components/AnswerCard/AnswerCard.vue'


export default defineComponent({
  name: 'QADetail',
  components: {
    AnswerCard
  },
  setup() {
    const answer = () => {

    }

    return {
      answer
    }
  },
})
</script>

<style lang="scss" scoped>
.content {
  background-color: #e0e4e5;
  padding-bottom: 100px;

  .question {
    background-color: #fff;
    width: 100%;
    height: 20vh;
    padding: 20px;
    box-sizing: border-box;

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
  }

  .answer {
    margin-top: 30px;

    .answer-title {
      font-size: 18px;
      font-weight: 700;
      margin: 0 0 20px 20px;
    }

    .answer-list {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  }

  .bottom {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 80px;
    background-color: #fff;
    display: flex;
    justify-content: space-around;
    align-items: center;

    .star {
      padding-left: 20px;
      width: 200px;
      box-sizing: border-box;
      display: flex;
      align-items: center;

      img {
        width: 20px;
        height: 20px;
        margin-right: 5px;
      }

      span {
        color: #949899;
      }
    }

    .answer-btn {
      background-color: #ff7744;
      width: 120px;
      height: 40px;
      border-radius: 20px;
      text-align: center;
      line-height: 40px;
      color: #fff;
    }
  }
}
</style>