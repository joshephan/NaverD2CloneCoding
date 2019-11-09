<template>
  <article>
    <figure class="image is-circle">
      <img :src="program.img" alt="">
    </figure>
    <div class="right-side">
      <img :src="program.title" alt="" class="title-image">
      <p>{{program.content}}</p>
      <a :href="program.link" class="link" target="_blank">사이트 바로가기</a>
    </div>
  </article>
</template>
<script>
export default {
  props: {
    program: {
      type: Object,
      default: {
        title: '',
        content: '',
        img: '',
        link: ''
      }
    }
  }
}
</script>
<style lang="scss" scoped>
article {
  display: flex;
  max-width: 810px;
  margin-bottom: 40px;
  figure.image {
    width: 224px;
    height: auto;
  }
  .right-side {
    padding: 22px 0 0 50px;
  }
  .title-image {
    margin-bottom: 15px;
  }
  p {
    color: #666;
  }
  .link {
    margin-top: 13px;
    padding: 0 20px 0 22px;
    color: #00c374;
    border: 1px solid #00c374;
    height: 35px;
    font-size: 14px;
    line-height: 35px;
    border-radius: 17.5px;
    display: inline-block;
  }
}
</style>