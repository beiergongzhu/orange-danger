<template>
  <view class="content" @click="navigateToPage(navigateUrl)">
    <view class="iconImg">
      <img :src="icon" alt="Icon">
    </view>
    <view class="text">
      <view class="title">{{ title }}</view>
      <view class="sub">点击立刻进行识别</view>
    </view>
    <view class="navigateIcon">
      <img src="@/static/arrow-right.png" alt="Icon">
    </view>
  </view>
</template>

<script lang="ts">
import {
  defineComponent,
  ref
} from 'vue'

export default defineComponent({
  name: "ToolItem",
  props: {
    icon: String,
    title: String,
    navigateUrl: String
  },
  setup(props) {
    const { icon, title, navigateUrl } = props

    const navigateToPage = (navigateUrl: string) => {
      uni.navigateTo({
        url: navigateUrl
      })
    }

    return {
      icon,
      title,
      navigateToPage,
      navigateUrl
    }
  }
})

</script>

<style scoped>
.content {
  background-color: white;
  width: 94vw;
  height: 14vh;
  border-radius: 40px;
  box-shadow: 0 3px 3px lightgray;
  display: flex;
  /* justify-content: space-around; */
  align-items: center;
  padding: 0 24px;
  box-sizing: border-box;
}

.iconImg {
  width: 60px;
  height: 60px;
}

.iconImg img {
  width: 100%;
  height: 100%;
}

.navigateIcon {
  width: 40px;
  height: 40px;
}

.navigateIcon img {
  width: 100%;
  height: 100%;
}

.text {
  width: 42vw;
  height: 60px;
  display: flex;
  flex-direction: column;
  margin: 8px 30px 0 20px;
}

.title {
  text-align: center;
  color: orange;
  font-weight: 700;
  font-size: 20px;
}

.sub {
  text-align: center;
  color: #787c7d;
  font-size: 12px;
  margin-top: 4px;
}
</style>
