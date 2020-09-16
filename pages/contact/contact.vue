<template>
	<view class="contact">
		<image class="img" src="http://www.itcast.cn/2018czydz/images/gywmban.jpg"></image>
		<view class="info">
			<view @click="callMe">联系电话：176-0529-2122(点击拨打)</view>
			<view>联系地址：圣诞岛</view>
		</view>
		<map class="map" :longitude="longitude" :latitude="latitude" :scale="scale" :markers="markers"></map>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				longitude: 112.600243,
				latitude: 31.178114,
				scale: 14,
				markers: [
					{
						longitude: 112.600243,
						latitude: 31.178114,
						iconPath: '../../static/lemon.png',
						width: 30,
						height: 30
					}
				]
			}
		},
		methods: {
			callMe() {
				uni.makePhoneCall({
					phoneNumber: '176-0529-2122'
				})
			}
		}
	}
</script>

<style lang="scss">
	.contact {
		.img {
			width: 750rpx;
			height: 320rpx;
		}
		.info {
			padding: 10rpx 20rpx;
			font-size: 30rpx;
			view {
				line-height: 80rpx;
				border-bottom: 1px solid #eee;
			}
		}
		.map {
			width: 750rpx;
			height: 750rpx;
		}
	}
</style>
