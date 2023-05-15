<script setup>
// 1.定义props
defineProps({
  title: {
    type: String,
    default: "默认标题"
  },
  subtitle: {
    type: String,
    default: "默认子标题"
  }
})
  
</script>

<template>
    <div class="area-header">
      <h3 class="title">{{ title }}</h3>
      <div class="description">{{ subtitle }}</div>
    </div>
</template>

<style lang="less" scoped>
   .area-header {
      margin-bottom: 30px;
      .title {
        margin-bottom: 20px;
        color: #000;
      }
      .description {
        font-size: 13px;
        color: #008c8c;
      }
    }
</style>


