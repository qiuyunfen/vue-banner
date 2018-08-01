<template>
    <Banner @click.native="doSomething()" ref="swipers">
        <!-- <template v-for="item in activityList" slot-scope="props" :slot="item.id">
            <activity-item :key="item.id" :img-src="item.img" :content="item.content"  :status="item.status" :id="item.id" class="swiper-slide"></activity-item>
        </template> -->
    </Banner>
</template>
<script>
    import Banner from '../components/Banner.vue'

    export default {
        name: 'ActivityList',
        components: {
            Banner
        },
        methods: {
            doSomething() {
                window.console.log(this.$refs.swipers);
                window.console.log(this.$refs.swipers.$refs.swiper.swiper.realIndex);
            }
        },
        data: function () {
            return {
                activityList: [
                    {
                        id: 1,
                        img: require('./../imgs/1.jpg'),
                        content: '截止时间2018.07.02',
                        status: 'proccess',
                    }
                ]
            }
        }
    }
    
</script>
