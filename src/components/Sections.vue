<template>
	<div class="section  container">
		<div class="title">
			<h2 class="text_h2">——发现话题——</h2>
			<small>发现生活的美，找到属于自己的兴趣</small>
		</div>
		<ul class="list">
			<li v-for="(item,index) in section" :key="index"  @mouseenter="enter(index)" @mouseleave="leave(index)">
				    <a  :style='{backgroundImage:"url("+ item.src +")"}'></a>
				<div class="mask"  v-show="isShow==index">
					<div class="info-wrap">
						<div class="bound-effect">
							<i class="lt"></i>
							<i class="rt"></i>
							<i class="lb"></i>
							<i class="rb"></i>
						</div>
						<div class="text-middle">
							<h3 class="text_h3">{{item.msg.h}}</h3>
							<p>{{item.msg.p}}</p>
						</div>
					</div>
				</div>
			</li>
		</ul>
	</div>
</template>
<script>
	export default {
	  name: 'header',
	  data () {
    return {
	      isToggle: false,
	      isShow: -1
    }
  },
  methods: {
    enter: function (index) {
	      this.isShow = index
    },
	    leave: function () {
	      this.isShow = -1
    }

  },
	  props: {
	    section: {
	      type: Array,
	      default: []
    }
  }
	
	}
</script>
<style lang='less' scoped>
	.section {
		margin-top: 60px;
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
			display: flex;
			justify-content: center;
			flex-wrap: wrap;
			width: 100%;
			li {
				width: 100%;
				flex: 1 1 30%;
				margin: 0.6em 1.2em;
				position: relative;
				height: 280px;
				cursor: pointer;
				 a {
					display: inline-block;
					width: 100%;
				  height: 100%;
					background-size: cover;
					background-position: 50%;
					background-repeat: no-repeat;
				}
				.mask {
					position: absolute;
					transition: opacity ease-in .2s;
					left: 0;
					top: 0;
					width: 100%;
					height: 100%;
					background: rgba(125, 125, 125, 0.7);
					.info-wrap {
						position: absolute;
						left: 50%;
						top: 50%;
						width: 74%;
						height: 164px;
						margin-left: -37%;
						margin-top: -82px;
						.bound-effect {
							position: absolute;
							left: 0;
							top: 0;
							width: 100%;
							height: 100%;
							z-index: 2;
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
							width: 100%;
							height: 50%;
							color: #fff;
							h3 {
								width: 100%;
								font-size: 2em;
								font-weight: normal;
							}
							p {
								width: 100%;
								font-size: 1.6em;
							}
						}
					}
				}
			}
		}
	}

	@media screen and (max-width:767px) {
		.container {
			width: 100%!important;
			.text_h2 {
				font-size: 20px !important;
				// margin-bottom: 10px !important;
			}
			li{
				height: 150px!important;
			}
			.mask{
				// height: 65%!important;
			
			small {
				font-size: 12px !important;
			}
			a {
				width: 150px!important;
				height:150px!important;
			}
			.bound-effect {
				height: 60%!important;
				top: 20%!important;
		 	}
		}
			.text-middle {
				.text_h3 {
					font-size: 12px!important;
					margin-top: 50%;
				}
				p {
					font-size: 8px!important;
				}
			}
		}
	}
</style>
