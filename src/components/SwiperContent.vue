<template>

    <div class="activuty-box swiper-slide">
        <img :src="require('../imgs/'+imgSrc)" class="activity-img"/>
        <div v-if="isEnd" class="activity-end-footer">
            <img src="../imgs/page-1@2x.png" class="activity-end-picture"/>
        </div>
        <div class="activity-footer" v-else>
            <p class="end-time-box">{{content}}</p>
        </div>

    </div>
</template>
<script>
    export default {
        name: 'SwiperContent',
        props: {
            imgSrc: {
                type: String,
                required: true
            },
            content: {
                type: String,
                required: true
            },
            status: {
                type: String,
                required: true
            }
        },
        computed: {
            isEnd() {
                return this.status == "end"
            }
        }
    }
</script>

<style>
.activuty-box {
    position: relative;
    width: 345px;
    height: 88px;
    border-radius: 4px;
    background-color: #d8d8d8;
}
.activity-img {
    width:100%;
    height: 100%;
}
.activity-footer {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 246px;
    height: 18px;
    border-radius: 5px;
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.4));;
}
    .end-time-box {
        margin: 0;
        padding: 3px 11px 3px 0;
        text-align: right;
        font-size: 12px;
        line-height: 12px;
        color: #ffffff;
    }
    .activity-end-footer {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0.7;
        border-radius: 4px;
        background-color: #000000;
    }
    .activity-end-picture {
        width: 77px;
        height: 65px;
        position: absolute;
        top: 13px;
        right: 11px;
    }
</style>