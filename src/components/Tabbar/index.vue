<template>
  <view>
    <van-tabbar :active="tabbarActive">
      <van-tabbar-item
        v-for="(item, index) in tabbarList"
        :key="index"
        :dot="item.dot_status"
        @click="handleTabbar(item)"
      >
        <image
          slot="icon"
          :src="item.icon"
          mode="aspectFit"
          style="width: 60upx; height: 60upx;"
        />
        <image
          slot="icon-active"
          :src="item.icon_active"
          mode="aspectFit"
          style="width: 60upx; height: 60upx;"
        />
        {{ item.name }}
      </van-tabbar-item>
    </van-tabbar>
  </view>
</template>

<script>
import VanTabbar from "@/wxcomponents/vant/tabbar/index";
import VanTabbarItem from "@/wxcomponents/vant/tabbar-item/index";

export default {
  data() {
    return {
      task_status: true,
      menu_status: true,
      tabbarActive: 0,
      tabbarList: [
        {
          name: "首页",
          icon: "../../static/tabbar/home.png",
          icon_active: "../../static/tabbar/home.png",
          url: "/pages/index/index",
          dot_status: false,
        },
        {
          name: "任务",
          icon: "../../static/tabbar/task.png",
          icon_active: "../../static/tabbar/task.png",
          url: "/pages/task/index",
          dot_status: true,
        },
        {
          name: "菜单",
          icon: "../../static/tabbar/menu.png",
          icon_active: "../../static/tabbar/menu.png",
          url: "/pages/menu/index",
          dot_status: true,
        },
        {
          name: "我的",
          icon: "../../static/tabbar/me.png",
          icon_active: "../../static/tabbar/me.png",
          url: "/pages/personal-center/index",
          dot_status: false,
        },
      ],
    };
  },
  components: {
    VanTabbar,
    VanTabbarItem,
  },
  onLoad() {},
  methods: {
    handleTabbar(item) {
      console.log(item.url);
      uni.navigateTo({
        url: item.url
      });
    },
  },
};
</script>

<style lang="less"></style>
