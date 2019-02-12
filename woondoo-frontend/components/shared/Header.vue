<template>
  <nav class="main-nav" :class="{'is-white': isWhite}">
    <div class="main-nav__inner full-width clearfix" >
      <NuxtLink to="/" class="logo">
        운두교회
      </NuxtLink>
      
      <div class="menu">
        <NuxtLink to="/greeting">
            교회소개
        </NuxtLink>
        <NuxtLink to="/sermons">
            설교
        </NuxtLink>
        <NuxtLink to="/notice">
            나눔 및 소식
        </NuxtLink>
        <NuxtLink to="/map">
            오시는 길
        </NuxtLink>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: ['isWhite'],
}
</script>

<style lang="scss" scoped>
.main-nav {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  z-index: 9;
}

.main-nav .main-nav__inner {
  position: relative;
  height: 80px;
} 

.main-nav .main-nav__inner .logo {
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  max-width: 50px;
  white-space: nowrap;
  display: block;
  font-weight: bold;
  color: #000;
  font-size: 24px;
}

.main-nav.is-white .main-nav__inner .logo {
  color: #fff;
}

.main-nav .main-nav__inner .menu {
  display: table;
  float: right;
  height: 100%;
}

.main-nav .main-nav__inner .menu > a {
  display: table-cell;
  vertical-align: middle;
  padding-left: 20px;
  padding-right: 20px;
  position: relative;
  font-weight: bold;
  color: #000;
  font-size: 18px;
}

.main-nav.is-white .main-nav__inner .menu > a {
  color: #fff;
}

.main-nav .main-nav__inner .menu > a .submenu {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  text-align: center;
}
</style>

