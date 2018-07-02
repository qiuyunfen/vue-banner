<template>
    <swiper :options="swiperOption">
        <swiper-slide>
            <swiper-content img-src="1.jpg" content="截止日期2018.07.02" status="end"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content img-src="2.jpg" content="截止日期2018.07.02" status="process"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content img-src="3.jpg" content="截止日期2018.07.02" status="end"></swiper-content>
        </swiper-slide>
        <swiper-slide>
            <swiper-content img-src="4.jpg" content="截止日期2018.07.02" status="end"></swiper-content>
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
                centeredSlides: true,
                autoplay: {
                    delay: 2500,
                    disableOnInteraction: false
                },
                slidesPerView: 1.09,
                spaceBetween: 10,
                loop : true
            }
        }
    }
}
</script>