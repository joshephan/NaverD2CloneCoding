<template>
  <footer>
    <div class="footer-box">
      <ul class="img-link">
        <li>
          <a href="http://developers.naver.com/" target="_blank" class="link-1">NAVER Developers</a>
        </li>
        <li>
          <a href="http://colloq.naver.com/" target="_blank" class="link-2">NAVER Colloquium</a>
        </li>
        <li>
          <a href="http://deview.kr/" target="_blank" class="link-3">DEVIEW</a>
        </li>
        <li>
          <a href="http://naver.github.io/" target="_blank" class="link-4">OpenSource</a>
        </li>
        <li>
          <a href="http://www.d2startup.com/" target="_blank" class="link-5">D2 STARTUP FACTORY</a>
        </li>
      </ul>
      <ul class="social-link">
        <li>
          <a href="mailto:d2@navercorp.com">
            <b-icon icon="email" />
          </a>
        </li>
        <li>
          <a href="http://facebook.com/naverd2" target="_blank">
            <b-icon icon="facebook" />
          </a>
        </li>
        <li>
          <a href="http://d2.naver.com/d2.atom" target="_blank">
            <b-icon icon="rss" />
          </a>
        </li>
      </ul>
    </div>
    <div class="footer-box">
      <p>이 사이트는 <a href="https://d2.naver.com/home" target="_blank">NAVER D2</a>를 클론 코딩한 사이트입니다.</p>
    </div>
  </footer>
</template>
<style lang="scss" scoped>
footer {
  background: #f9f9f9;
}
.footer-box {
  display: flex;
  justify-content: center;
  align-items: center;
  &:first-child {
    padding: 43px 0px;
    border-bottom: 1px solid #efefef;
  }
  &:nth-child(2) {
    padding: 19px 0;
    color: #323232;
    font-size: 16px;
    word-spacing: 2px;
    line-height: 10px;
    font-family: tahoma,Helvetica,sans-serif;
    max-width: 1180px;
    margin: 0 auto;
  }
}
.img-link li {
  display: inline-block;
  margin-right: 50px;
  vertical-align: middle;
  a {
    overflow: hidden;
    display: block;
    background: url(https://d2.naver.com/static/img/app/sp_program_logo_v2.png) no-repeat;
    background-size: 335px 160px;
    color: transparent;
    line-height: 100px;
  }
  .link-1 {
    width: 137px;
    height: 17px;
    background-position: 0 -86px;
  }
  .link-1 {
    width: 137px;
    height: 17px;
    background-position: 0 -86px;
  }
  .link-2 {
    width: 131px;
    height: 14px;
    background-position: 0 -124px;
  }
  .link-3 {
    width: 131px;
    height: 14px;
    background-position: 0 -124px;
  }
  .link-4 {
    width: 105px;
    height: 24px;
    background-position: -229px -52px;
  }
  .link-5 {
    width: 79px;
    height: 22px;
    background-position: -229px -80px;
  }
}
.social-link {
  min-width: 300px;
  text-align: right;
  li {
    display: inline-block;
    margin-left: 15px;
    a {
      color: #a5a5a5;
      &:hover {
        color: #555;
      }
    }
  }
}
</style>