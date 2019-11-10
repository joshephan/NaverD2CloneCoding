<template>
  <article>
    <div class="article-container">
      <div class="text-container">
        <h1 class="article-title">{{item.title}}</h1>
        <p class="content">{{item.content}}</p>
        <div class="metadata">
          <b-icon icon="clock-outline" size="is-small"></b-icon>
          <span>{{item.createdAt}}</span>
          <b-icon icon="eye" size="is-small"></b-icon>
          <span>{{item.viewCount}}</span>
        </div>
      </div>
      <figure class="image thumbnail">
        <img :src="item.thumbnail" alt />
      </figure>
    </div>
  </article>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      default: {
        id: "",
        title: "",
        createdAt: "",
        viewCount: 0,
        thumbnail: ""
      }
    }
  }
};
</script>
<style scoped>
article {
  margin: 0 auto 30px;
}
.article-container {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #ededed;
}
.article-title {
  font-size: 24px;
  color: #434a53;
  padding-bottom: 14px;
}
.text-container {
  max-width: 640px;
}
.content {
  font-size: 14px;
  line-height: 20px;
  max-height: 40px;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
  margin-bottom: 15px;
  color: #666;
}
.metadata {
  font-size: 12px;
  color: #b5b5b5;
  font-family: Avenir, "Lato", "애플 SD 산돌고딕 Neo", "Apple SD Gothic Neo",
    "나눔바른고딕", NanumBarunGothic, "나눔고딕", NanumGothic, "맑은 고딕",
    "Malgun Gothic", "돋움", dotum, AppleGothic, sans-serif;
  overflow: hidden;
  padding: 7px 0;
  padding-bottom: 30px;
  width: 100%;
}
.thumbnail {
  width: 170px;
}
</style>