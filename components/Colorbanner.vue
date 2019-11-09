<template>
  <section :style="{backgroundColor: bgColor}">
    <p>
      {{title}}
      <span class="bar">&nbsp;</span>
      <span class="description">{{text}}</span>
    </p>
  </section>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default:""
    },
    text: {
      type: String,
      default:""
    },
    bgColor: {
      type: String,
      default:""
    }
  }
}
</script>
<style scoped>
section {
  height: 150px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
p {
  font-size: 26px;
  color: #fff;
}
.bar {
  display: inline-block;
  width: 1px;
  margin: 0 20px;
  background-color: #fff;
  opacity: 0.2;
}
.description {
  font-size: 17px;
}
@media (max-width:767px) {
  .description {
    display: none;
  }
}
</style>