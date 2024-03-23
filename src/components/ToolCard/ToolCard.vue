<template>
  <view class="content">
    <ToolItem v-for="item in data" :key="item.id" :icon="item.icon" :title="item.title" :navigateUrl="item.navigateUrl" />
  </view>
</template>

<script lang="ts">
import {
  defineComponent,
  ref
} from 'vue'
import ToolItem from "@/components/ToolCard/ToolItem/ToolItem.vue";

export default defineComponent({
  name: "ToolCard",
  components: {
    ToolItem
  },
  setup() {
    const data = [{
      title: '拍照识别病虫害',
      icon: '../../../static/icon/camera.png',
      navigateUrl: '/pages/BugScan/BugScan',
      id: 1
    },
      // {
      //   title: '解决措施',
      //   icon: '../../../static/icon/methodIcon.png',
      //   navigateUrl: '/pages/BugSearch/BugSearch',
      //   id: 2
      // },
    ]

    return {
      data
    }
  }
})

</script>

<style scoped>
@import "./index.css";
</style>