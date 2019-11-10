<template>
  <section class="email-box">
    <form action="/" method="POST">
      <b-icon icon="email" size="is-small" class="email-btn"></b-icon>
      <input type="email" placeholder="이메일 주소 입력" />
      <input type="submit" value="구독하기" />
    </form>
  </section>
</template>
<script>
export default {
  data() {
    return {
      isFocus: false
    };
  }
};
</script>
<style lang="scss" scoped>
.email-box {
  color: #a0a0a0;
  margin-top: 36px;
  font-size: 14px;
}
.email-btn {
  position: absolute;
  margin: 7px 0 0 7px;
  color: #a0a0a0;
  font-size: 14px;
}
input {
  font-size: 12px;
}
input[type=email] {
  width: 185px;
  height: 30px;
  border: 1px solid #d3d3d3;
  border-radius: 3px;
  padding: 0 10px 0 37px;
  vertical-align: top;
  color: #a0a0a0;
  background: url(https://d2.naver.com/static/img/app/bg_input_email.png) 0 0
    repeat-y;
  &:hover {
    border: 1px solid #a0a0a0;
    color: #6e6e70;
    background: url(https://d2.naver.com/static/img/app/bg_input_email2.png) 0 0
      repeat-y;
  }
}
input[type=submit] {
  width: 60px;
  height: 30px;
  color: #fff;
  border-radius: 3px;
  -webkit-appearance: none;
  background: #a0a0a0;
  border: 0;
}
</style>