<template>
  <section>
    <h1 class="year">
      {{item.year}}
    </h1>
    <section class="event" v-for="event in item.list" :key="event.title">
      <a :href="event.link">{{event.linkTitle}}</a>
      <div class="circle"></div>
      <div class="divider"></div>
      <p>
        {{event.date}}
        <br>
        <span v-html="event.title"></span>
      </p>
    </section>
  </section>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      default: {
        year: null,
        list: [{
          title: null,
          date: null,
          link: null,
          linkTitle: null
        }],
      }
    }
  }
}
</script>
<style lang="scss" scoped>
.event {
  display: flex;
  justify-content: center;
  height: 120px;
  align-items: center;
}
.year {
  width: 80px;
  height: 80px;
  margin: 0 auto;
  border-radius: 40px;
  background-color: #32cda0;
  font-size: 24px;
  color: #fff;
  letter-spacing: -2px;
  line-height: 80px;
  text-align: center;
  z-index: 20;
}
.circle {
  width: 100px;
  height: 40px;
  background: url(https://d2.naver.com/static/img/app/about/about_dot.png) no-repeat 0 0;
  background-size: 20px 20px;
  margin: 0 30px;
  background-position-x: center;
  background-position-y: 10px;
  position: relative;
  z-index: 1;
}
.divider {
  position: absolute;
  height: inherit;
  width: 1px;
  background: #999;
  transform: translateX(-50%);
  left: 50%;
  z-index: 0;
}
a {
  width: 500px;
  display: block;
  color: #1cba8c;
  padding-right: 50px;
  font-size: 25px;
  font-weight: normal;
  text-align: right;
  &:hover {
    text-decoration: underline;
  }
}
p {
  padding-left: 50px;
  color: #555;
  font-size: 14px;
  width: 500px;
  text-align: left;
}
</style>