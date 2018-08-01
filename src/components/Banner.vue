<!--@TODO:-->
<!--2.进一步抽象：外面传入一个object然后渲染出来，而不需要自己做循环-->
<!--3.迁移到项目中-->

<!--img-src：图片的地址，必须需要require；-->
<!--content：这是在swiper的底下的字的信息-->
<!--status：活动是否已经结束（"end"）;-->
<!--class: 在swiper情况下，必须为swiper-slide-->
<template>
    <swiper :options="swiperOption" @click.native="doSomething()" ref="swiper">
        <!-- <template v-for="item in activityList">
            <slot :name="item.id"></slot>
        </template> -->
        <div class="swiper-slide">Slide 1</div>
        <div class="swiper-slide">Slide 2</div>
        <div class="swiper-slide">Slide 3</div>
        <div class="swiper-slide">Slide 4</div>
        <div class="swiper-slide">Slide 5</div>
        <div class="swiper-slide">Slide 6</div>
        <div class="swiper-slide">Slide 7</div>
        <!-- <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide>
        <swiper-slide>Slide 5</swiper-slide>
        <swiper-slide>Slide 6</swiper-slide>
        <swiper-slide>Slide 7</swiper-slide>
        <swiper-slide>Slide 8</swiper-slide>
        <swiper-slide>Slide 9</swiper-slide>
        <swiper-slide>Slide 10</swiper-slide> -->
    </swiper>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
import 'swiper/dist/css/swiper.css'

// 最底层封装的是vue-awesome-swiper,地址：https://github.com/surmon-china/vue-awesome-swiper
export default {
    name: 'Banner',
    components: {
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
                slidesPerView: 1.08, // slidesPerView：一页显示多少的slides，设置分数就出现了两侧都有一点出来
                loopedSlides: 20, // loopedSlides：设置20是为了让在slides尽头后面还有连续的slides,这个dom最多是现有的总活动的数量的三倍，所以并不会影响到性能
                spaceBetween: 10, // spaceBetween: 两个slides的间隔
                loop : true // loop: 是不是无限循环播放
            }
        }
    },
    methods: {
        doSomething() {
            window.console.log(111)
            window.console.log(this.$refs.swiper)
            // window.console.log(this.$refs.swiper.swiper.activeIndex)
            // window.console.log(this.$refs.swiper.swiper.realIndex)
            // window.console.log(this.$refs.swiper.swiper)
        }
    }
}
</script>