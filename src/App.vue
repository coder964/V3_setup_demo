<script setup> 
  import highScore from "./data/high_score.json"
  import RoomArea from "./components/RoomArea.vue";

</script>

<template>
  <div class="app">
    <!-- 1.高评价模块 -->
    <room-area :area-data="highScore"/>
  </div>
</template>

<style lang="less" scoped>
  .app {
    width: 1032px;
    padding: 40px;
    margin: 0 auto;
  }
</style>
