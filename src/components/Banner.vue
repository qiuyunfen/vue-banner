<!--@TODO:-->
<!--2.进一步抽象：外面传入一个object然后渲染出来，而不需要自己做循环-->
<!--3.迁移到项目中-->

<!--img-src：图片的地址，必须需要require；-->
<!--content：这是在swiper的底下的字的信息-->
<!--status：活动是否已经结束（"end"）;-->
<!--class: 在swiper情况下，必须为swiper-slide-->
<template>

    <swiper :options="swiperOption">
        <swiper-slide>
            <activity-item :img-src="require('../imgs/1.jpg')" content="截止日期2018.07.02"  status="processing" class="swiper-slide"/>
        </swiper-slide>
        <swiper-slide>
            <activity-item :img-src="require('../imgs/2.jpg')" content="截止日期2018.07.02" status="processing"  class="swiper-slide"/>
        </swiper-slide>
        <swiper-slide>
            <activity-item :img-src="require('../imgs/3.jpg')" content="截止日期2018.07.02" status="end" class="swiper-slide"/>
        </swiper-slide>
    </swiper>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
import ActivityItem from './ActivityItem'
import 'swiper/dist/css/swiper.css'

// 最底层封装的是vue-awesome-swiper,地址：https://github.com/surmon-china/vue-awesome-swiper
export default {
    name: 'Banner',
    components: {
        ActivityItem,
        swiper,
        swiperSlide
    },
    data() {
        return {
            swiperOption: {
                centeredSlides: true,
                autoplay: { // autoplay: 自动播放
                    delay: 3000,
                    disableOnInteraction: false //当设置为false时，用户操作之后autoplay不会被禁掉
                },
                slidesPerView: 1.09, // slidesPerView：一页显示多少的slides，设置分数就出现了两侧都有一点出来
                loopedSlides: 20, // loopedSlides：设置20是为了让在slides尽头后面还有连续的slides
                spaceBetween: 10, // spaceBetween: 两个slides的间隔
                loop : true // loop: 是不是无限循环播放
            }
        }
    }
}
</script>