<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view>
			<text class="title">{{title}}</text>
		</view>
		<van-button color="#7232dd">单色按钮</van-button>
		<van-button color="#7232dd" plain>单色按钮</van-button>
		<van-button color="linear-gradient(to right, #4bb0ff, #6149f6)">渐变色按钮</van-button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				 active: 'home',
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
