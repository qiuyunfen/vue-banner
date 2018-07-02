<template>
    <swiper>
        <swiper-slide>
            <swiper-content img-src="ending.png" content="截止日期2018.07.02"></swiper-content>
        </swiper-slide>
        <swiper-slide><img src="../imgs/2.jpg"/></swiper-slide>
        <swiper-slide><img src="../imgs/3.jpeg"/></swiper-slide>
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
    }
}
</script>