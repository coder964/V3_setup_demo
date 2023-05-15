<script setup>
  const Props = defineProps({
    itemValue: {
      type: Object,
      default: () => ({})
    }
  })
</script>

<template>
  <div class="item">
    <img class="picture_url" :src="itemValue.picture_url" alt="">
    <div class="verify_info">
      <template v-for="value in itemValue.verify_info.messages" :key="value">
        <span>{{ value }}</span>
      </template>
    </div>
    <div class="name">
      <span>
        {{ itemValue.name }}
      </span>
    </div>
    <div class="price">
      <span>{{ itemValue.price_format }}</span>
      <span>/晚</span>
    </div>
    <div class="bottom_info">
      <span>{{ itemValue.bottom_info.content }}</span>
    </div>
  </div>
</template>

<style lang="less" scoped>
.item {
  width: 334px;
  margin: 0 15px 15px 0;

  .picture_url {
    width: 100%;
  }

  .verify_info {
    margin-bottom: 5px;

    span {
      margin-right: 5px;
      color: #767676;
      font-size: 12px;
    }
  }

  .name {
    display: -webkit-box;
    -webkit-line-clamp: 2; //设置的行数
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;

    margin-bottom: 5px;
    font-size: 15px;
    font-weight: bold;
  }

  .price {
    font-size: 12px;
    color: #008489;
    margin-bottom: 5px;
  }

  .bottom_info {
    font-size: 15px;
    color: #767676;
  }
}</style>
