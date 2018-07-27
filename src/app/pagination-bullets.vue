<template>
      <!-- swiper -->
      <swiper :options="swiperOption">
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide>
        <swiper-slide>Slide 5</swiper-slide>
        <swiper-slide>Slide 6</swiper-slide>
        <swiper-slide>Slide 7</swiper-slide>
        <swiper-slide>Slide 8</swiper-slide>
        <swiper-slide>Slide 9</swiper-slide>
        <swiper-slide>Slide 10</swiper-slide>
        <div class="swiper-pagination swiper-pagination-bullets pagination" slot="pagination"></div>
      </swiper>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
import 'swiper/dist/css/swiper.css'

  export default {
      components: {
        swiper,
        swiperSlide
    },
    data() {
      return {
        swiperOption: {
          pagination: {
            el: '.swiper-pagination',
            clickable: true,
            renderBullet(index, className) {
              return `<span class="${className} swiper-pagination-bullet-custom">${index + 1}</span>`
            }
          }
        }
      }
    }
  }
</script>

<style>
 .swiper-pagination-bullet-custom {
    width: 20px;
    height: 20px;
    text-align: center;
    line-height: 20px;
    font-size: 12px;
    color: red;
    opacity: 1;
    background: rgba(0,0,0,0.2);
  }
  .swiper-pagination-bullet-custom.swiper-pagination-bullet-active {
    color: #fff;
    background: #007aff;
  }
  .pagination {
      position: relative;
  }
</style>