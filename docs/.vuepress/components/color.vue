<template>
  <div class="card">
    <div class="container">
      <span class="color-list" v-for="item of colorList" :key="item.class">
        <div class="color" :class="`bg-${item.class}${getColorI(item2)}`" v-for="item2 of 11" :key="item2">
          {{ `${item.class}${getColorI(item2)}` }}
        </div>
      </span>
    </div>
  </div>
</template>

<script lang="js">
  import 'help-code-fastly/src/style/color.css'
  export default {
    data() {
      return {
        colorList: [
          { text: '红', class: 'red' },
          { text: '粉红', class: 'pink' },
          { text: '紫', class: 'purple' },
          { text: '深紫', class: 'deep-purple' },
          { text: '靛', class: 'indigo' },
          { text: '蓝', class: 'blue' },
          { text: '浅蓝', class: 'light-blue' },
          { text: '青', class: 'cyan' },
          { text: '茶', class: 'teal' },
          { text: '绿', class: 'green' },
          { text: '浅绿', class: 'light-green' },
          { text: '青柠', class: 'lime' },
          { text: '黄', class: 'yellow' },
          { text: '琥珀', class: 'amber' },
          { text: '橙', class: 'orange' },
          { text: '深橙', class: 'deep-orange' },
          { text: '棕', class: 'brown' },
          { text: '灰', class: 'grey' },
          { text: '蓝灰', class: 'blue-grey' }
        ]
      }
    },
    methods: {
      getColorI(i) {
        return i === 1 ? '' : `-${i - 1}`
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .container {
    color: black;
    margin: -16px 0 0 -16px;
    .color-list {
      margin: 16px 0 0 16px;
      display: inline-block;
      width: 110px;
      .color {
        height: 50px;
        border-radius: 4px;
        line-height: 50px;
        text-align: center;
        font-size: 14px;
      }
    }
  }
</style>
