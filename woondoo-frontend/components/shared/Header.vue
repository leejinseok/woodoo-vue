<template>
  <nav class="main-nav">
    <div class="main-nav__inner full-width clearfix">
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
}
</script>

