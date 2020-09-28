<template>
  <view>
    <van-cell-group>
      <van-field
        :value="username"
        label="用户名"
        placeholder="请输入用户名"
        error
      />
      <van-field
        :value="phone"
        label="手机号"
        placeholder="请输入手机号"
        error-message="手机号格式错误"
        :border="false"
      />
      <van-field
        :value="message"
        label="留言"
        type="textarea"
        placeholder="请输入留言"
        autosize
        :border="false"
      />
    </van-cell-group>
  </view>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      phone: "",
      message: "",
    };
  },
  components: {},
  onLoad() {},
  methods: {},
};
</script>

<style lang="less"></style>
