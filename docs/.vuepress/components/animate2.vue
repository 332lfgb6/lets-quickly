<template>
  <div>
    <button @click="data.unshift(`item-${currentI++}`)">添加</button>
    <transition-group name="fadeLeft" tag="ul">
      <li v-for="item in data" :key="item">
        {{ item }}
      </li>
    </transition-group>
  </div>
</template>
<script lang="js">
  import 'help-code-fastly/src/animate/index.scss'
  export default {
    components: {},
    data() {
      return {
        currentI: 0,
        data: []
      }
    }
  }
</script>
<style scoped>
  .fadeLeft-move {
    transition: transform 1s ease;
  }
</style>
