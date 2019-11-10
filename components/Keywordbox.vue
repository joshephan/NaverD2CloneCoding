<template>
  <section>
    <h3>TOP KEYWORDS</h3>
    <div class="tag-cover">
      <div class="tag is-inline-block" v-for="(i, j) in item" :key="j">{{i}}</div>
    </div>
  </section>  
</template>
<script>
export default {
  data() {
    return {
      item: ['JavaScript', '빅데이터', '분산처리', 'Golang', 'Scala']
    }
  }
}
</script>
<style scoped>
h3 {
  font-family: Roboto,sans-serif;
  font-size: 18px;
  font-weight: 500;
  color: #000;
}
.tag-cover {
  padding: 21px 0 22px;
  border-bottom: 1px solid #ececec;
}
.tag {
  overflow: hidden;
  display: inline-block;
  max-width: 205px;
  height: 32px;
  margin: 0 6px 9px 0;
  padding: 0 18px;
  border-radius: 15.5px;
  background-color: #f2f5f7;
  font-size: 14px;
  color: #666;
  line-height: 32px;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>