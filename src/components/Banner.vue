<template>
    <swiper :options="swiperOption">
        <swiper-slide>
            <swiper-content img-src="1.jpg" content="截止日期2018.07.02"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content img-src="2.jpg" content="截止日期2018.07.02"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content img-src="3.jpg" content="截止日期2018.07.02"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content img-src="4.jpg" content="截止日期2018.07.02"></swiper-content>
        </swiper-slide>

    </swiper>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
import SwiperContent from './SwiperContent.vue'
import 'swiper/dist/css/swiper.css'

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
                centeredSlides: false,
                autoplay: {
                    delay: 2500,
                    disableOnInteraction: false
                }
            }
        }
    }
}
</script>