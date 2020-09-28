<template>
  <view class="personal">
    <view class="personal-box">
      <view class="personal-box-top">
        <view>
          <van-image
            lazy-load
            use-loading-slot
            custom-class="personal-box-top-img"
            src="https://img.yzcdn.cn/vant/cat.jpeg"
          >
            <van-loading slot="loading" type="spinner" size="20" vertical />
          </van-image>
        </view>
        <view class="personal-box-top-user">
          <view class="personal-box-top-user-name">天才码农阿星呀</view>
          <view class="personal-box-top-user-edit" @click="handleUserInfo">编辑资料</view>
        </view>
      </view>
      <view class="personal-box-overview">
        <view class="personal-box-overview-item">
          <view class="personal-box-overview-item-num">1097</view>
          <view class="personal-box-overview-item-txt">已连续打卡</view>
        </view>
        <view class="personal-box-overview-item">
          <view class="personal-box-overview-item-num">200</view>
          <view class="personal-box-overview-item-txt">记账总天数</view>
        </view>
        <view class="personal-box-overview-item">
          <view class="personal-box-overview-item-num">300</view>
          <view class="personal-box-overview-item-txt">记账总笔数</view>
        </view>
      </view>
      <view class="personal-box-list">
        <view class="personal-box-list-item">
          <view class="personal-box-list-item-con">
            <view class="personal-box-list-item-con-pic">
              <van-image
                custom-class="personal-box-list-item-con-pic-diy"
                src="../../../static/personal/fm.png"
              />
            </view>
            <view class="personal-box-list-item-con-txt">成员管理</view>
          </view>
          <view class="personal-box-list-item-con">
            <view class="personal-box-list-item-con-pic">
              <van-image
                custom-class="personal-box-list-item-con-pic-diy"
                src="../../../static/personal/visitor.png"
              />
            </view>
            <view class="personal-box-list-item-con-txt">访客管理</view>
          </view>
          <view class="personal-box-list-item-con">
            <view class="personal-box-list-item-con-pic">
              <van-image
                custom-class="personal-box-list-item-con-pic-diy"
                src="../../../static/personal/menu.png"
              />
            </view>
            <view class="personal-box-list-item-con-txt">菜品管理</view>
          </view>
          <view class="personal-box-list-item-con">
            <view class="personal-box-list-item-con-pic">
              <van-image
                custom-class="personal-box-list-item-con-pic-diy"
                src="../../../static/personal/task.png"
              />
            </view>
            <view class="personal-box-list-item-con-txt">任务管理</view>
          </view>
        </view>
      </view>
      <copyright />
    </view>
  </view>
</template>

<script>
import Copyright from "@/components/Copyright/index";
export default {
  data() {
    return {};
  },
  components: {
    Copyright,
  },
  onLoad() {},
  methods: {
    handleUserInfo() {
      uni.navigateTo({
        url: "/pages/user/edit/index"
      })
    }
  },
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
    height: 280upx;
    background-color: #fcd133;
    z-index: 2;
  }
  &-box {
    position: relative;
    z-index: 3;
    padding: 0 40upx;
    &-top {
      display: flex;
      &-img {
        border: 4upx solid #fff;
        width: 90upx;
        height: 90upx;
        border-radius: 90upx;
        image {
          border-radius: 50%;
        }
      }
      &-user {
        padding-left: 20upx;
        &-name {
          font-weight: 700;
          font-size: 34upx;
        }
        &-edit {
          margin-top: 10upx;
          font-size: 26upx;
          color: #ffeba2;
        }
      }
    }
    &-overview {
      display: flex;
      justify-content: space-between;
      padding: 0 20upx;
      &-item {
        margin-top: 20upx;
        text-align: center;
        &-num {
          font-size: 26upx;
          font-weight: 700;
        }
        &-txt {
          margin-top: 10upx;
          font-size: 24upx;
        }
      }
    }
    &-list {
      &-item {
        margin-top: 30upx;
        border-radius: 16upx;
        padding: 20upx;
        background-color: #fff;
        display: flex;
        justify-content: space-between;
        font-size: 24upx;
        text-align: center;
        &-con {
          &-pic {
            &-diy {
              width: 44upx;
              height: 44upx;
            }
          }
          &-txt {
            margin-top: 6upx;
          }
        }
      }
    }
  }
}
</style>
