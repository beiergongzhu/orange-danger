<template>
  <view class="content">
    <view class="scroll">
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
      <UserQAItem />
    </view>
  </view>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import UserQAItem from "./UserQAItem.vue";

export default defineComponent({
  name: "UserQAView",
  components: {
    UserQAItem,
  },
  setup() {

  },
});
</script>

<style lang="scss" scoped>
.content {
  margin-top: 20px;

  .scroll {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    height: 100%;
    overflow: scroll;
  }

}
</style>
