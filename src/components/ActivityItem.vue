<template>
<div>
    <div class="activuty-box" v-on:click="activityClickEvent">
        <div :style="{backgroundImage: 'url(' + imgSrc + ')'}" class="activity-img"></div>
        <div v-if="isEnd" class="activity-end-footer">
            <img src="../imgs/page-1@2x.png" class="activity-end-picture"/>
        </div>
        <div class="activity-footer" v-else>
            <p class="end-time-box">{{content}}</p>
        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ActivityItem",
  props: {
    id: {
      type: Number,
      required: true
    },
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
      required: true,
      default: "processing"
    }
  },
  data() {
      return {
        reqanimationreference: Function
      }
  },
  computed: {
    isEnd() {
      return this.status === "end";
    }
  },
  methods: {
    activityClickEvent() {
       this.reqanimationreference = window.requestAnimationFrame(this.repeatOften);
    },

    // repeatOften() {
    //     window.screenTop = window.screenTop+ 10
    //     console.log(window.screenTop)
    //     this.reqanimationreference = window.requestAnimationFrame(this.repeatOften);
    // },
    // stopStop () {
    //     cancelAnimationFrame(this.reqanimationreference)
    // }
  }
};
</script>

<style>

.activuty-box {
  position: relative;
  width: 100%;
  height: 88px;
  border-radius: 4px;
}

.activity-img {
  /*display: block;*/
  background-position: center center;
  border-radius: 4px;
  background-size: 100% auto;
  background-repeat: no-repeat;
}

.activity-footer {
  position: absolute;
  bottom: 1px;
  right: 10px;
  width: 246px;
  height: 18px;
  border-radius: 4px;
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    rgba(0, 0, 0, 0.4)
  );
}

.end-time-box {
  margin: 0;
  padding: 3px 11px 3px 0;
  text-align: right;
  font-size: 12px;
  line-height: 12px;
  color: #ffffff;
  letter-spacing: normal;
}

.activity-end-footer {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
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