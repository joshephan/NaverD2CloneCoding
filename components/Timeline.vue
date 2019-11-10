<template>
  <section>
    <div class="timeline">
      <div class="timeline-head">
        <img src="https://d2.naver.com/static/img/app/about/history_subtitle.png" alt />
        <p>개발자들을 위한 탁월한 지식과 경험을 공유하며 함께 성장합니다!</p>
      </div>
      <div class="timeline-body">
        <h1>History</h1>
        <History v-for="(item, i) in historyList" :key="i" :item="item" />
        <img class="logo" src="https://d2.naver.com/static/img/app/about/about_d2_img.png" width="100%" alt="d2">
      </div>
    </div>
  </section>
</template>
<script>
import History from '@/components/card/History.vue' 
import histories from '@/assets/data/history.json'

export default {
  components: {
    History
  },
  computed: {
    historyList() {
      return histories.list;
    }
  }
};
</script>
<style lang="scss" scoped>
section {
  background-color: #f7f7f9;
}
.timeline {
  width: 100%;
  max-width: 1180px;
  margin: 0 auto;
  padding-top: 50px;
  text-align: center;
}
.timeline-head {
  max-width: 760px;
  margin: 0 auto;
  padding: 33px 0 31px;
  p {
    margin-top: 13px;
    font-family: NanumSquare;
    font-size: 18px;
    color: rgba(103, 103, 103, 0.8);
    text-align: center;
    line-height: 28px;
  }
}
.timeline-body {
  max-width: 840px;
  margin: 0 auto;
  padding: 50px 0 45px;
  h1 {
    font-size: 36px;
    margin-bottom: 40px;
    color: #434a53;
    font-family: NanumSquare;
  }
}
.logo {
  width: 40px;
  height: 40px;
  margin: 25px auto;
}
</style>