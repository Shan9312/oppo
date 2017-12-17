<template>
  <div class='my-slide container' >
    <div class="title">
			<h2 class="text_h2">——O粉活动——</h2>
			<small>O粉活动</small>
		</div>
     <swiper :options="swiperOption">
        <swiper-slide v-for='(item,index) in slidesImg' :key='index'>
          <a :href="item.url" class='bgimg' :style='{background:"url("+ item.src+")"}'></a>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
      <div class='container' >
        <div class="title">
          <h2 class="text_h2">——APP下载——</h2>
          <small>更多奇妙玩法，激活自己</small>
        </div>
        <div class="imgs"><img src="../assets/img/15126998018372.jpg" alt=""></div>
      </div>
  </div>
</template>

<script>
  export default{
    name: 'slide',
    data () {
      return {
        swiperOption: {
          slidesPerView: 3,
          spaceBetween: 30,
          loop: true,
          autoplay: true,
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          }
        }
      }
    },
    props: {
      slidesImg: {
        type: Array,
        default: []
      }
    },
    computed: {
      swiper () {
        return this.$refs.mySwiper.swiper
      }
    },
    methods: {
      handleChange () {
        // TODO 当图片是黑色的那张时，切换后面背景为白色
        // console.dir(this.swiper && this.swiper.activeIndex)
        // console.dir(this.$refs.mySwiper.swiper)
        this.$emit('updateWhite', this.$refs.mySwiper.swiper)
      }
    }
  }
</script>

<style lang='less' scoped>
  
	.title {
    text-align: center;
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
.my-slide{
  margin:80px auto;
  .bgimg{
    display: inline-block;
    height:260px;
    width:100%;
    background-position: center!important;
    background-size:cover!important;
  }
  .swiper-pagination{
    width:100%;
    height:50px;
    line-height: 50px;
  }
  .container{
     .imgs{
        margin:0 auto;
        width: 100%;
        text-align: center;
        img{
          width: 100%;
          height: 100%;
        }
     }
  }
  @media screen and (min-width:768px) and (max-width:991px){
     
  }
  @media screen and (max-width:767px){
    .bgimg{
      height:140px;
      width:100%;
    }
    .container{
      .imgs{
        margin:0 auto;
        width: 100%;
        text-align: center;
        img{
          width: 100%;
        }
     }
    }
  }
}
</style>

