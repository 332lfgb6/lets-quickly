<template>
  <div>
    <input v-model="first" />
    <select v-model="current">
      <option v-for="item of jjcc" :key="item">{{ item }}</option>
    </select>
    <input v-model="second" />
    = {{ result }}
  </div>
</template>

<script>
  import { add, sub, mul, div } from 'help-code-fastly'
  export default {
    data() {
      return {
        first: '',
        second: '',
        current: '+',
        jjcc: ['+', '-', '×', '÷']
      }
    },
    computed: {
      result() {
        switch (this.current) {
          case '+':
            return add(this.first, this.second)
          case '-':
            return sub(this.first, this.second)
          case '×':
            return mul(this.first, this.second)
          case '÷':
            return div(this.first, this.second)
        }
      }
    }
  }
</script>

<style scoped>
  .wrong {
    color: red;
  }
  .right {
    color: green;
  }
</style>
