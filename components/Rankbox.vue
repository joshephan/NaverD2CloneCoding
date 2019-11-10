<template>
  <section class="rank-box">
    <h3>TOP 5</h3>
    <ol>
      <li v-for="(item, i) in items" :key="i"><span>{{i + 1}}</span>{{item}}</li>
    </ol>
  </section>
</template>
<script>
export default {
  props: {
    items: {
      type: Array,
      default: []
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
ol {
  margin-bottom: 34px;
  padding: 18px 0 14px;
  border-bottom: 1px solid #ececec;
}
li {
  overflow: hidden;
  display: inline-block;
  max-width: 250px;
  font-size: 14px;
  color: #666;
  text-decoration: none;
  white-space: nowrap;
  text-overflow: ellipsis;
}
li > span {
  display: inline-block;
  margin-right: 16px;
  font-family: Roboto, sans-serif;
  font-size: 15px;
  font-weight: 600;
  color: #1f2124;
  vertical-align: middle;
}
</style>