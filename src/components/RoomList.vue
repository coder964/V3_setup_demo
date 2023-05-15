<script setup>
  import RoomItem from "./RoomItem.vue"

  // 1.定义Props
  defineProps({
    itemData: {
      type: Object,
      default: () => ({})
    }
  })
</script>

<template>
    <div class="room-list">
      <template v-for="item in itemData.list" :key="item.id">
        <room-item :item-value="item"/>     
      </template>
    </div>
</template>

<style lang="less" scoped>
  .room-list {
    display: flex;
    flex-wrap: wrap;
    margin-right: -15px;
  }
</style>
