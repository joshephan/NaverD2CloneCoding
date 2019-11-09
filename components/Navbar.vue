<template>
  <nav id="navbar">
    <b-navbar class="nav-container">
      <template slot="brand">
        <b-navbar-item class="brand-btn" tag="router-link" :to="{ path: '/' }">
          <img src="https://d2.naver.com/static/img/app/d2_logo.gif" alt="NAVAER D2" />
        </b-navbar-item>
      </template>
      <template slot="start">
        <b-navbar-item href="/helloworld">Hello world</b-navbar-item>
        <b-navbar-item href="/news">D2 News</b-navbar-item>
        <b-navbar-item href="/program">D2 Program</b-navbar-item>
        <b-navbar-item href="/about">About D2</b-navbar-item>
      </template>
      <template slot="end">
        <b-navbar-item tag="div">
          <div class="is-flex">
            <b-input placeholder="D2에서 검색"></b-input>
            <b-icon class="search" icon="magnify"></b-icon>
          </div>
        </b-navbar-item>
      </template>
    </b-navbar>
  </nav>
</template>
<style lang="scss" scoped>
#navbar {
  display: flex;
  justify-content: center;
  height: 68px;
}
.navbar-item {
  color: #a0a0a0;
  transition: all .3s ease;
  padding: 8px 15px;
  &:hover {
    color: #000;
    background: transparent;
  }
}
.nav-container {
  max-width: 1100px;
  margin: 0 40px;
  width: 100%;
}
.brand-btn {
  margin-left: 50px;
}
.search {
  border-left: 1px solid #e7e7e7;
  margin-left: 16px;
  width: 43px;
  height: 34px;
  color: #a5a5a5;
}
</style>