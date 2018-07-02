<template>
    <swiper>
        <swiper-slide><img src="../imgs/1.jpg"/></swiper-slide>
        <swiper-slide><img src="../imgs/2.jpg"/></swiper-slide>
        <swiper-slide><img src="../imgs/3.jpeg"/></swiper-slide>
    </swiper>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'

import 'swiper/dist/css/swiper.css'

export default {
    name: 'Banner',
    components: {
        swiper,
        swiperSlide
    }
}
</script>