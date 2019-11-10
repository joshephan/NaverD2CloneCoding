<template>
  <section class="schedule">
    <div class="schedule-head">
      <h3>2019 주요 일정</h3>
      <button
        v-scroll-to="{
        el: '.timeline',
        duration: 500,
        easing: 'linear',
        force: true,
        cancelable: true,
        x: false,
        y: true}"
      >D2 히스토리 바로가기</button>
    </div>
    <div class="schedule-body">
      <Card v-for="(item, i) in schedules" :key="i" :item="item" />
    </div>
  </section>
</template>
<script>
import Card from "@/components/card/Schedule";
import scheduleList from "../assets/data/schedule.json";

export default {
  components: {
    Card
  },
  computed: {
    schedules() {
      return scheduleList.list;
    }
  },
  methods: {
    scrollToHistroy() {
      var target = this.$el.querySelector(".timeline");
      console.log(target);
      // window.scrollTo(0, target.offsetTop);
    }
  }
};
</script>
<style lang="scss" scoped>
.schedule {
  width: 100%;
  max-width: 840px;
  margin: 15px auto 60px;
  padding-top: 50px;
}
.schedule-head {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  h3 {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    font-size: 30px;
    color: #1f2124;
    letter-spacing: -1.7px;
    text-align: center;
  }
  button {
    height: 32px;
    padding: 0 12px 0 11px;
    background-color: #fff;
    border: 1px solid #e0e0e0;
    font-size: 14px;
    color: #1f2124;
    letter-spacing: -0.5px;
    -webkit-appearance: none;
    cursor: pointer;
  }
}
.schedule-body {
  margin-top: 35px;
  border-top: 2px solid #2b2b2b;
}
</style>