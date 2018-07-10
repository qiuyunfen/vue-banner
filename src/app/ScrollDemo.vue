<template>
    <div style="height:2000px;">
        <button id="test" style="position:fixed;right:0;bottom:0" @click="clickEvent">回到顶部</button>
    </div>
</template>
<script>
export default {
    methods: {
        clickEvent() {
            document.body.scrollTop = document.documentElement.scrollTop = 0;
        }
    }
}
</script>

