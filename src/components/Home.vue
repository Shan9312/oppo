<template>
  <div class="home">
    <my-header :title='titleArr'></my-header>
    <my-slide :slides='slideItems' @updateWhite='handleUpdate'></my-slide>
    <my-section :section='sectionImg'></my-section>
    <my-slides :slides='slideItems'></my-slides>
  </div>
</template>

<script>
  import myHeader from './Header'
  import mySlide from './Slide'
  import mySection from './Sections'
  import mySlides from './Slide_2.vue'
  export default {
    name: 'home',
    data () {
      return {
        titleArr: [
          {
            label: '首页',
            url: 'https:www.baidu.com'
          },
          {
            label: '消息',
            url: 'http:www.baidu.com'
          },
          {
            label: '话题',
            url: 'http:www.baidu.com'
          },
          {
            label: '动态',
            url: 'http:www.baidu.com'
          },
          {
            label: '官网',
            url: 'http:www.baidu.com'
          }
        ],
        slideItems: [
          {
            bg: require('../assets/img/slide1.jpg'),
            url: 'http://hd.oppo.com/act/m/jietou/index.html'
          },
          {
            bg: require('../assets/img/slide2.jpg'),
            url: 'https://hd.oppo.com/act/m/2017/xingfuxiaowu/index.html'
          },
          {
            bg: require('../assets/img/slide3.jpg'),
            url: 'https://www.oppo.cn/thread-170161646-1'
          }
        ],
        sectionImg: [
          {
            src: require('../assets/img/main1.jpg'),
            msg: {
              h: '周杰伦的2000W个故事',
              p: '5210万人参与'
            }
          },
          {
            src: require('../assets/img/mian2.jpg'),
            msg: {
              h: '我走过的街头',
              p: '28.0万人参与'
            }
          },
          {
            src: require('../assets/img/main3.jpg'),
            msg: {
              h: '幸福的小物管',
              p: '27.0万人参与'
            }
          },
          {
            src: require('../assets/img/main4.jpg'),
            msg: {
              h: '少女心博物馆',
              p: '18.0万人参与'
            }
          },
          {
            src: require('../assets/img/main5.jpg'),
            msg: {
              h: '看见的问道',
              p: '8.0万人参与'
            }
          },
          {
            src: require('../assets/img/main6.jpg'),
            msg: {
              h: '夜夜夜夜',
              p: '20.0万人参与'
            }
          }
        ],
        white: false
      }
    },
    components: {
      myHeader, mySlide, mySection, mySlides
    },
    methods: {
      handleUpdate (value) {
        console.dir(value.snapIndex)
        if (value.snapIndex === 4) {
          this.white = true
        } else {
          this.white = false
        }
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
