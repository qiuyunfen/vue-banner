<template>
    <Banner :activityList="activityList" @activity-click-event="activityClickEvent">
        <template v-for="item in activityList" slot-scope="props" :slot="item.id">
            <activity-item :key="item.id" :img-src="item.img" :content="item.content"  :status="item.status" :id="item.id" class="swiper-slide"></activity-item>
        </template>
    </Banner>
</template>
<script>
    import Banner from '../components/Banner.vue'
    import ActivityItem from '../components/ActivityItem.vue'

    export default {
        name: 'ActivityList',
        components: {
            Banner,
            ActivityItem
        },
        methods: {
            activityClickEvent(props) {
                window.console.log("in the acivityList", props);
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
                    }, {
                        id: 2,
                        img: require('./../imgs/2.jpg'),
                        content: '截止时间2018.07.02',
                        status: 'end',
                    }
                ]
            }
        }

    }
</script>
