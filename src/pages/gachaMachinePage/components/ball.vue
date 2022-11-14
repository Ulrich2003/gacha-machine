<template>
  <div>
    <div class="blue-ball" v-if="color == 'blue'">
      <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/bg2-8-4.png" />
    </div>
    <div class="red-ball" v-if="color == 'red'">
      <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/box-chose21.png" />
    </div>
    <div class="yellow-ball" v-if="color == 'yellow'">
      <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/box-chose31.png" />
    </div>
    <div class="purple-ball" v-if="color == 'purple'">
      <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/bg2-9-2.png" />
    </div>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps(["color"]);
</script>

<style lang="scss" scoped>
.blue-ball {
  width: 100%;
  height: 100%;
  background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/pop3.png");
  background-size: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    $size: 70%;
    width: $size;
    height: $size;
  }
}

.yellow-ball {
  width: 100%;
  height: 100%;
  background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/pop2.png");
  background-size: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    $size: 50%;
    width: $size;
    height: $size;
  }
}

.red-ball {
  width: 100%;
  height: 100%;
  background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/pop1.png");
  background-size: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    $size: 50%;
    width: $size;
    height: $size;
  }
}

.purple-ball {
  width: 100%;
  height: 100%;
  background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/pop4.png");
  background-size: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    $size: 50%;
    width: $size;
    height: $size;
  }
}
</style>
