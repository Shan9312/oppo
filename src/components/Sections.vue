<template>
	<div class="section  container">
		<div class="title">
			<h2 class="text_h2">——发现话题——</h2>
			<small>发现生活的美，找到属于自己的兴趣</small>
		</div>
		<ul class="list">
			<li>
				<a href=""><img src="../assets/img/1main.jpg" alt=""></a>
				<div class="mask">
					<div class="info-wrap">
						<i class="lt"></i>
						<i class="rt"></i>
						<i class="lb"></i>
						<i class="rb"></i>
					</div>
					<div class="text-middle">
						<h3 class="text_h3">周杰伦的2000W个故事</h3>
						<p>5210人参与</p>
					</div>
				</div>
			</li>
			<li>
				<a href=""><img src="../assets/img/1main.jpg" alt=""></a>
			</li>
			<li>
				<a href=""><img src="../assets/img/1main.jpg" alt=""></a>
			</li>
			<li>
				<a href=""><img src="../assets/img/1main.jpg" alt=""></a>
			</li>
			<li>
				<a href=""><img src="../assets/img/1main.jpg" alt=""></a>
			</li>
			<li>
				<a href=""><img src="../assets/img/1main.jpg" alt=""></a>
			</li>
		</ul>
		<br>
		<br>
		<br>
		<br>
		<br>
		<br>
		<br>
		<br>
		<br>
		<br>
		<br>
	</div>
</template>
<script>

</script>
<style lang='less' scoped>
	.section {
		margin-top: 100px;
		text-align: center;
		.title {
			h2 {
				color: #05b570;
				font-size: 36px;
				height: 36px;
				margin-bottom: 20px;
				font-weight: 400;
			}
			small {
				display: block;
				color: #666;
				font-size: 16px;
				margin-bottom: 20px;
			}
		}
		.list {
			width: 100%;
			display: flex;
			justify-content: center;

			flex-wrap: wrap;
			li {
				flex: 1 1 30%; 
				margin: 0.6em 1.2em;
				position: relative;
				a {
					display: inline-block;
					max-width: 100%;
					img {
						max-width: 100%;
					}
				}
				.mask {
					position: absolute;
					transition: opacity ease-in .2s;
					left: 0;
					top: 0;
					width: 100%;
					height: 100%;
					background: rgba(125, 125, 125, 0.7);
					.info-wrap,
					.text-middle {
						position: absolute;
						left: 50%;
						top: 50%;
						width: 74%;
						height: 100%;
						margin-left: -37%;
						margin-top: -82px;
						z-index: 1;
						color: #fff;
						text-align: center;
						display: table;
						i {
							position: absolute;
							width: 28px;
							height: 23px;
							border: 1px solid transparent;
							opacity: .4;
						}
						.lt {
							left: 0;
							top: 0;
							border-top-color: #fff;
							border-left-color: #fff;
						}
						.rt {
							right: 0;
							top: 0;
							border-top-color: #fff;
							border-right-color: #fff;
						}
						.lb {
							left: 0;
							bottom: 0;
							border-bottom-color: #fff;
							border-left-color: #fff;
						}
						.rb {
							right: 0;
							bottom: 0;
							border-bottom-color: #fff;
							border-right-color: #fff;
						}
					}
					.text-middle {
						text-align: center;
						h3 {
							color: #fff;
							width: 100%;
							font-size: 2.2em;
							font-weight: normal;
							margin-top: 58px;
						}
						p {
							width: 100%;
							margin-top: 10px;
							font-size: 1.6em;
						}
					}
				}
			}
		}
	}

	@media screen and (max-width:767px) {
		.container {
      .text_h2{
				font-size: 20px !important;
				margin-bottom: 10px !important;
			}
			small{
				font-size: 12px !important;
			}
			a {
				max-width: 240px;
			}
			.text_h3{
				font-size:12px!important;
			}
			p{
			  font-size:8px!important;	
			}
		}
	}
</style>
