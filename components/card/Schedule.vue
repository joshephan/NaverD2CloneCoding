<template>
  <article>
    <figure class="image">
      <img :src="item.img" alt />
    </figure>
    <div class="middle">
      <h4>{{item.title}}</h4>
      <p>{{item.content}}</p>
    </div>
    <div class="tail">
      <p class="date" v-html="item.date"></p>
      <a v-if="item.link" :href="item.link">바로가기</a>
    </div>
  </article>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      default: {
        title: null,
        content: null,
        date: null,
        link: null,
        img: null
      }
    }
  }
};
</script>
<style lang="scss" scoped>
article {
  display: flex;
  padding: 22px 0;
  border-bottom: 1px solid #e3e3e3;
}
figure {
  width: 170px;
  height: 120px;
}
.middle {
  padding-left: 24px;
  width: 460px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  h4 {
    font-size: 20px;
    color: #434a53;
    line-height: 28px;
    font-weight: bold;
    vertical-align: middle;
  }
  p {
    padding-top: 8px;
    font-size: 14px;
    color: #909090;
  }
}
.tail {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 14px;
  &:before {
    display: block;
    position: absolute;
    margin-left: -26px;
    width: 1px;
    height: 68px;
    background-color: #eee;
    content: "";
  }
  p {
    font-size: 14px;
    color: #555;
    line-height: 26px;
  }
  a {
    color: #1cba8c;
    font-size: 14px;
    text-decoration: underline;
  }
}
</style>