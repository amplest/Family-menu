<template>
  <view>
    <van-tabbar
      :active="tabbarActive"
      active-color="#07c160"
      inactive-color="#000"
      :change="onChange"
    >
      <van-tabbar-item
        name="home"
        icon="home-o"
      >首页</van-tabbar-item>
      <van-tabbar-item
        name="task"
        icon="balance-list-o"
      >任务</van-tabbar-item>
      <van-tabbar-item
        name="menu"
        icon="records"
      >菜谱</van-tabbar-item>
      <van-tabbar-item
        name="personal"
        icon="smile-o"
      >我的</van-tabbar-item>
    </van-tabbar>
  </view>
</template>

<script>
import VanTabbar from "@/wxcomponents/vant/tabbar/index";
import VanTabbarItem from "@/wxcomponents/vant/tabbar-item/index";
export default {
  components: {
    VanTabbar,
    VanTabbarItem,
  },
  data() {
    return {
      tabbarActive: "home",
    };
  },
  onChange(event) {
    console.log(event);
    this.setData({ tabbarActive: event.detail });
  },
  onLoad() {},
  methods: {},
};
</script>

<style lang="less">
</style>
