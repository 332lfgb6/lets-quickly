<template>
  <div class="container" ref="container">
    <div v-for="item of 50" :key="item">列表项{{ item }}</div>
  </div>
</template>

<script>
  import { scrollbar } from 'help-code-fastly'
  export default {
    mounted() {
      scrollbar.init(this.$refs.container, { alwaysShowTracks: true })
    }
  }
</script>

<style scoped>
  .container {
    width: 200px;
    height: 200px;
    overflow: auto;
  }
</style>
