<template>
    <body style="height:2000px;">
    <div id="box" class="box" @click="event">
        <div class="box-in"></div>
    </div>  
    </body>
</template>
<script>
export default {
    methods: {
        event() {
            var timer  = null;
            cancelAnimationFrame(timer);
                //获取当前毫秒数
                // var startTime = +new Date();     
                //获取当前页面的滚动高度
                
                // div.scrollTop = div.scrollHeight; 
                // var duration = 500;
                // var c = bodyTop;
                
                timer = requestAnimationFrame(function func(){
                    // var time = duration - Math.max(0,startTime - (+new Date()) + duration);
                    // document.documentElement.scrollTop = document.body.scrollTop = time * (-c) / duration + bodyTop;
                    // timer = requestAnimationFrame(func);
                    // if(time == duration){
                    //     cancelAnimationFrame(timer);
                    // }
                    var bodyTop = document.body.scrollTop || document.documentElement.scrollTop
                    document.documentElement.scrollTop = document.body.scrollTop = bodyTop + 10;

                    timer = requestAnimationFrame(func)
                    if(Math.abs(document.body.clientHeight - document.documentElement.clientHeight) <= (document.documentElement.scrollTop || document.body.scrollTop)) {
                        cancelAnimationFrame(timer);
                    }
                });
        },
        clickEvent() {
            document.body.scrollIntoView()
        }
    }
}
</script>

<style>
.box{
    position:fixed;
    right:10px;
    bottom: 10px;
    height:30px;
    width: 50px;    
    text-align:center;
    padding-top:20px;    
    background-color: lightblue;
    border-radius: 20%;
    overflow: hidden;
}
.box:hover:before{
    top:50%
}
.box:hover .box-in{
    visibility: hidden;
}
.box:before{
    position: absolute;
    top: -50%;
    left: 50%;
    transform: translate(-50%,-50%);
    content:'回到顶部';
    width: 40px;
    color:peru;
    font-weight:bold;

}    
.box-in{
    visibility: visible;
    display:inline-block;
    height:20px;
    width: 20px;
    border: 3px solid black;
    border-color: white transparent transparent white;
    transform:rotate(45deg);
}
</style>

