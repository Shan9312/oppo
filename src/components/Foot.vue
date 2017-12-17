<template>
	<div class="footer">
		<div class="container">
			<ul>
				<li>
					<h4>oppo社区</h4>
				</li>
				<li>oppo论坛</li>
				<li>oppo乐园</li>
				<li>oppo R9</li>
				<li>oppo R11s</li>
				<li></li>
			</ul>
			<ul>
				<li>
					<h4>友情链接</h4>
				</li>
				<li>oppo R11</li>
				<li>安卓游戏</li>
				<li>oppo 基地 </li>
				<li>魔趣安卓论坛</li>
				<!-- <li>UC浏览器</li> -->
			</ul>
			<ul class="list2">
				<li>
					<h4>oppo 论坛</h4>
				</li>
				<li>oppo Rs9</li>
				<li>ROM之家</li>
				<li>手机中国论坛</li>
				<li>安卓手机</li>
			</ul>
			<ul class="list3">
				<li>
					<h4>oppo 社区</h4>
				</li>
				<li>奇兔刷机</li>
				<li>Find7论坛</li>
				<li>oppo R11s</li>
				<li>ColorOS社区</li>
			</ul>
			<div>
				<h2>在线联系</h2>
				<h3>4001-666-888</h3>
				<p>24小时全国热线</p>
			</div>
		</div>
	</div>
</template>
<script>
	export default {

	}
</script>
<style scoped lang="less">
	.footer {
		background-color: #f5f5f5;
		width: 100%;
		height: 400px;
		color: #666;
		font-size: 16px;
		.container {
			height: 100%;
			display: flex;
			justify-content: space-between;
			ul {
				width: 20%;
				height: 80%;
				li {
					margin: 2px;
					padding: 5px;
					text-align: left;
					cursor: pointer;
					h4 {
						margin-bottom: 4px;
						font-size: 18px;
					}
				}
			}
			div {
				float: left;
				margin-top: 15px;
				text-align: center;
				h2 {
					padding: 10px 20px;
					border: 1px solid #666;
					color: #fff;
					border-radius: 10px;
					background: #666;
				}
			}
		}
	}

	@media screen and (max-width:767px) {
		// .list2,.list3{
		// 	display: none;
		// }
		.footer {
			background-color: #f5f5f5;
			width: 100%;
			height: 180px;
			color: #666;
			font-size: 8px;
			.container {
				height: 100%;
				ul {
					float: left;
					width: 20%;
					height: 80%;
					li {
						margin: 2px;
						padding: 3px;
						text-align: left;
						cursor: pointer;
						h4 {
							margin-bottom: 4px;
							font-size: 12px;
						}
					}
				}
				div {
					float: left;
					margin-top: 8px;
					text-align: center;
					h2 {
						padding: 5px 10px;
						border: 1px solid #666;
						color: #fff;
						border-radius: 5px;
						background: #666;
					}
				}
			}
		}
	}
</style>
