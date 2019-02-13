<template>
  <div>
    <ul>
      <li v-for="notice in notices" :key="notice.id">
        {{ notice.title }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: ['notices']
}
</script>
