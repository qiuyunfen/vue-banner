<!--img-src：图片的地址，必须需要require；-->
<!--content：这是在swiper的底下的字的信息-->
<!--status：活动是否已经结束（"end"）;-->
<!--class: 在swiper情况下，必须为swiper-slide-->
<template>
    <swiper :options="swiperOption">
        <swiper-slide>
            <swiper-content :img-src="require('../imgs/1.jpg')" content="截止日期2018.07.02"  status="processing" class="swiper-slide"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content :img-src="require('../imgs/2.jpg')" content="截止日期2018.07.02" status="processing"  class="swiper-slide"></swiper-content>
        </swiper-slide>
        <swiper-slide class="swiper-slide">
            <swiper-content :img-src="require('../imgs/3.jpg')" content="截止日期2018.07.02" status="end" class="swiper-slide"></swiper-content>
        </swiper-slide>
    </swiper>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
import SwiperContent from './SwiperContent.vue'
import 'swiper/dist/css/swiper.css'

// 最底层封装的是vue-awesome-swiper,地址：https://github.com/surmon-china/vue-awesome-swiper
// 在这个项目组中，我们会使用几个api设置：
// autoplay: 自动播放
// slidesPerView：一页显示多少的slides，设置分数就出现了两侧都有一点出来
// loopedSlides：设置999是为了让在slides尽头后面还有连续的slides
// spaceBetween: 两个slides的间隔
// loop: 是不是无限循环播放
export default {
    name: 'Banner',
    components: {
        swiper,
        swiperSlide,
        SwiperContent
    },
    data() {
        return {
            swiperOption: {
                centeredSlides: true,
                autoplay: {
                    delay: 3000,
                    disableOnInteraction: false
                },
                slidesPerView: 1.09,
                loopedSlides: 9999,
                spaceBetween: 10,
                loop : true
            }
        }
    }
}
</script>