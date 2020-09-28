<template>
  <view class="personal">
    <view class="personal-box">
      <view class="personal-box-top">
        <view>
          <van-image
            round
            lazy-load
            use-loading-slot
            width="5rem"
            height="5rem"
            src="https://img.yzcdn.cn/vant/cat.jpeg"
          >
          <van-loading slot="loading" type="spinner" size="20" vertical />
          </van-image>
        </view>
        <view>
          <view>天才码农阿星呀</view>
          <view>编辑</view>
        </view>
      </view>
      <view class="personal-box-overview">
        23
        123123123
        23123123
        23123123
        2312312323123123231231232312312323123123231231232312312323123123231231232312312323123123
      </view>
      <view class="personal-box-list">
        12312313 </view>
      <view class="personal-box-copy"> 1563456456
<br>231231232312312323123123231231232312312323123123

      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {};
  },
  components: {},
  onLoad() {},
  methods: {},
};
</script>

<style lang="less">
.personal {
  position: relative;
  z-index: 1;
  &:before {
    content: "";
    position: absolute;
    top: 0;
    width: 100%;
    height: 350upx;
    background-color: #fcd133;
    z-index: 2;
  }
  &-box {
    position: relative;
    z-index: 3;
    padding: 0 40upx;
    &-top {
    }
    &-list {
    }
  }
}
</style>
