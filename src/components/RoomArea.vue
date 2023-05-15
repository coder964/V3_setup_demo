<script setup>
  import AreaHeader from "./AreaHeader.vue"
  import RoomList from "./RoomList.vue"

  // 定义Props
  defineProps({
    areaData: {
      type: Object,
      default: () => ({})
    }
  })
  
</script>

<template>
  <!-- 1. 区域header -->
  <area-header :title="areaData.title" :subtitle="areaData.subtitle"/>

  <!-- 2. 房间列表 -->
  <room-list :item-data="areaData"/>
</template>

<style lang="less" scoped>

</style>
