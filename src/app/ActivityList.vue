<template>
    <Banner :activityList="activityList"></Banner>
</template>
<script>
import Banner from '../components/Banner.vue'

export default {
    name: 'ActivityList',
    components: {
        Banner
    },
    data: function () {
        return {
            activityList: [
                {
                    id: 1,
                    img: require('../imgs/1.jpg'),
                    content: '截止时间2018.07.02',
                    status: 'proccess'
                }, {
                    id: 2,
                    img: require('../imgs/2.jpg'),
                    content: '截止时间2018.07.02',
                    status: 'end'
                }
            ]
        }
    }
   
}
</script>
