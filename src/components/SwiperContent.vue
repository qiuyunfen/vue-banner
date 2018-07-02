<template>
    <div>
        <img :src="imgSrc"/>
        <div>
            <p>{{content}}</p>
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