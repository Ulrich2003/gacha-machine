<template>
  <div class="page">
      <img src="../../assets/static/topimg.jpg" class="bg"/>
      <GachaMachine class="gachaMachine"/>
  </div>
</template>

<script setup lang="ts">
import GachaMachine from './components/gachaMachine.vue'
import { ref } from 'vue'
</script>

<style scoped lang="scss">
.page{
  position: relative;
  .bg{
    position: absolute;
    top: 0;
    width: 100%;
    z-index: 100;
  }
  .gachaMachine{
    position: absolute;
    width: 100%;
    z-index: 200;
  }
}
</style>
