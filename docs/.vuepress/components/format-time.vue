<template>
  <div>
    <div>当前时间：{{ time }}</div>
    <div>格式化后：{{ formatedTime }}</div>
  </div>
</template>

<script>
  import { formatTime } from 'help-code-fastly'
  export default {
    data() {
      return {
        time: new Date()
      }
    },
    computed: {
      formatedTime() {
        return formatTime(this.time)
      }
    },
    created() {}
  }
</script>

<style scoped>
  .time {
    color: red;
  }
</style>
