<template>
	<view class="news">
		<newsItem @itemClick="goDetail" :list="newsList"></newsItem>
	</view>
</template>

<script>
	import newsItem from '../../components/news-item/news-item.vue'
	export default {
		data() {
			return {
				newsList: []
			}
		},
		components: {
			newsItem
		},
		methods: {
			async getNews() {
				const res = await this.$myRequest({
					url: '/api/getnewslist'
				})
				this.newsList = res.data.message
			},
			goDetail(id) {
				console.log(id)
				uni.navigateTo({
					url: '/pages/news-detail/news-detail?id='+id
				})
			}
		},
		onLoad() {
			this.getNews()
		}
	}
</script>

<style lang="scss">
	.news {
		
	}
</style>
