<template>
	<view class="music-header">
		<view v-if="icon" class="music-header-icon">
			<text @tap="handleToBack" class="iconfont icon-zuojiantou"></text> | <text @tap="handleToHome" class="iconfont icon-shouye"></text>
		</view>
		{{ title }}
	</view>
</template>

<script>
	export default {
		name:"musicHeader",
		props: ['title', 'icon'],
		data() {
			return {
				
			};
		},
		methods: {
			handleToBack() {
				uni.navigateBack()
			},
			handleToHome() {
				uni.navigateTo({
					url: "/pages/index/index"
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
.music-header{
	width: 100%;
	height: 75px;
	font-size: 16px;
	line-height: 80px;
	text-align: center;
	position: relative;
	.music-header-icon{
		position: absolute;
		left: 8px;
		top: 26px;
		width: 90px;
		height: 30px;
		line-height: 31px;
		background: rgba(0,0,0,0.4);
		border-radius: 15px;
		color: white;
		display: flex;
		justify-content: space-evenly;
	}
}
</style>
