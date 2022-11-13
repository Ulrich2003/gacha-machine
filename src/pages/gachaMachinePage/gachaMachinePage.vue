<template>
  <div class="page">
    <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/topimg.jpg" class="bg" />
    <GachaMachine class="gachaMachine" />
    <!-- 底部图片 -->
    <div class="bottombg">
      <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/bottombg.png" />
    </div>
  </div>
</template>

<script setup lang="ts">
import GachaMachine from "./components/gachaMachine.vue";
</script>

<style scoped lang="scss">
.page {
  position: relative;
  .bg {
    position: absolute;
    top: 0;
    width: 100%;
    z-index: 100;
  }
  .gachaMachine {
    position: absolute;
    width: 100%;
    z-index: 200;
  }

  .bottombg {
    position: absolute;
    z-index: 300;
    top:400vw;
    width: 100%;
    img {
      width: 100%;
    }
  }
}
</style>
