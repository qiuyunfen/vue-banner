<template>

    <div class="activuty-box">
        <img :src="require('../imgs/'+imgSrc)" class="activity-img"/>
        <div class="activity-footer">
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
        width: 100%;
        height: 100%;
    }

    .activity-footer {
        position: absolute;
        bottom: 0;
        right: 0;
        width: 100%;
        height: 18px;
    }

    .end-time-box {
        margin: 0;
        padding: 3px 11px 3px 0;
        text-align: right;
        font-size: 12px;
        line-height: 12px;
        color: #ffffff;
    }
</style>