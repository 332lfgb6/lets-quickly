<template>
  <div>
    <button @click="follow">关注</button>
    <div>
      关注成功
      <span class="count">X {{ count }}</span>
    </div>
  </div>
</template>

<script>
  import { throttle } from 'help-code-fastly'
  export default {
    data() {
      return {
        count: 1
      }
    },
    methods: {
      follow() {
        throttle(() => {
          this.count++
        }, 1000)
      }
    }
  }
</script>

<style scoped>
  .count {
    color: green;
  }
</style>
