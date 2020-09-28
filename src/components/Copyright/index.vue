<template>
  <view>
    <view class="copyright">{{ text }}</view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      text: "FAMILY MENU",
    };
  },
  components: {},
  onLoad() {},
  methods: {},
};
</script>

<style lang="less">
.copyright {
  text-align: center;
  color: rgba(69, 90, 100, 0.6);
  margin-top: 30upx;
  font-size: 24upx;
}
</style>
