<template>
  <div class="card">
    <div class="title">观沧海</div>
    <div class="author">曹操</div>
    <div class="content">东临碣石，以观沧海。 水何澹澹，山岛竦峙。 树木丛生，百草丰茂。 秋风萧瑟，洪波涌起。 日月之行，若出其中； 星汉灿烂，若出其里。 幸甚至哉，歌以咏志。</div>
  </div>
</template>

<script>
  export default {}
</script>

<style lang="stylus" scoped>
  .card {
    margin-top: 16px;
    width: 300px;
    padding: 16px;
    border: 1px solid rgba(0, 0, 0, 0.12);
    .title {
      font-size: 16px;
      font-weight: bold;
    }
    .author {
      font-size: 12px;
      margin: 8px 0;
      text-align: right;
      color: #333;
    }
    .content {
      font-size: 14px;
      color: #666;
    }
  }
</style>
