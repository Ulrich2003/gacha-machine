<template>
  <div>
    <div class="blue-ball" v-if="color == 'blue'">
      <img src="../../../assets/static/bg2-8-4.png" />
    </div>
    <div class="red-ball" v-if="color == 'red'">
      <img src="../../../assets/static/box-chose21.png" />
    </div>
    <div class="yellow-ball" v-if="color == 'yellow'">
      <img src="../../../assets/static/box-chose31.png" />
    </div>
    <div class="purple-ball" v-if="color == 'purple'">
      <img src="../../../assets/static/bg2-9-2.png" />
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
  background: url("../../../assets/static/pop3.png");
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
  background: url("../../../assets/static/pop2.png");
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
  background: url("../../../assets/static/pop1.png");
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
  background: url("../../../assets/static/pop4.png");
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
