<script setup> 
  import { ref } from "vue"
  import RoomArea from "./components/RoomArea.vue";

  // 模拟在服务器获取数据(不会立刻拿到，而是会等一会儿)
  const highScore = ref({})
  setTimeout(() => {
    // 因为是通过inport函数导入的，它会将high_score.json文件作为一个模块导入了，所以需要通过default属性来拿到数据
    import("./data/high_score.json").then((res) => {
      console.log(res.default);
      highScore.value = res.default
    })
  }, 1000)

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
