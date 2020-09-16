<template>
	<view class="goods_list">
		<view class="goods_item" v-for="item in goods" :key="item.id" @click="navigator(item.id)">
			<image :src="item.img_url"></image>
			<view class="price">
				<text>￥{{item.sell_price}}</text>
				<text>￥{{item.market_price}}</text>
			</view>
			<view class="name">
				<text>{{item.title}}</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: ['goods'],
		methods: {
			navigator(id) {
				this.$emit('goodsItemClick', id)
			}
		}
	}
</script>

<style lang="scss">
	.goods_list {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		padding: 0 16rpx;
		.goods_item {
			background-color: #fff;
			width: 355rpx;
			margin: 10rpx 0;
			padding: 16rpx;
			box-sizing: border-box;
			image {
				width: 80%;
				height: 150px;
				display: block;
				margin: auto;
			}
			.price {
				color: $shop-color;
				font-size: 36rpx;
				margin: 20rpx 0 6rpx 0;
				text:nth-child(2) {
					color: #ccc;
					font-size: 28rpx;
					margin-left: 18rpx;
					text-decoration: line-through;
				}
			}
			.name {
				font-size: 28rpx;
				line-height: 50rpx;
				padding-bottom: 16rpx;
				padding-top: 10rpx;
			}
		}
	}
</style>
