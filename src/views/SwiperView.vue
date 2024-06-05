<template>
  <div style="padding: 0 16px">
    <t-swiper
      direction="vertical"
      :height="192"
      :autoplay="true"
      @change="handleChange"
      :interval="3000"
    >
      <t-swiper-item v-for="(item, index) in swiperList" :key="index">
        {{ item }}
      </t-swiper-item>
    </t-swiper>
  </div>
</template>

<script lang="ts" setup>
const swiperList = [
  "曹操",
  "刘备",
  "孙权",
  "诸葛亮",
  "司马懿",
  "周瑜",
  "吕布",
  "貂蝉",
  "关羽",
  "赵云",
  "张飞",
];
const handleChange = (index: number, context: any) => {
  console.log("基础示例,页数变化到》》》", index, context);
};
</script>
