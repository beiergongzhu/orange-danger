<template>
  <view class="forum">
    <van-tabs v-model:active="active" @click="onClickTab" sticky swipeable :ellipsis="false" :swipe-threshold="3"
      title-active-color="black" color="#ffa500" background="#ccc">
      <van-tab v-for="  item   in   data  " :title="item.title" :key="item.title">
        <UserQAView v-if="active === 0" />
        <HotArticle v-if="active === 1" />
      </van-tab>
    </van-tabs>
  </view>
</template>

<script lang="ts">
import {
  defineComponent,
  ref
} from 'vue'
// 导入需要用到的组件
import HotArticle from "@/components/TechnologyForum/HotArticle/HotArticle.vue"
import UserQAView from "@/components/TechnologyForum/UserQAView/UserQAView.vue"

export default defineComponent({
  name: 'TechnologyForum',
  components: {
    HotArticle,
    UserQAView
  },
  setup() {
    // 头部导航栏数据
    const data = [{
      title: '问答',
      index: 0
    }, {
      title: '热门文章',
      index: 1
    }]

    // 选中标志，用于切换内容组件
    let active = ref(0);

    interface ChangeData {
      detail: {
        index: number
      }
    }
    // 切换内容组件函数
    const onClickTab = (data: ChangeData) => {
      console.log(data);
      active.value = data.detail.index
    }

    return {
      data,
      active,
      onClickTab
    }
  }
})

</script>

<style scoped></style>
