<template>
  <div class="page">
    <div class="star">
      <img src="../../../assets/static/star-left.png" />
      <img src="../../../assets/static/star-right.png" />
    </div>
    <div class="machine">
      <img
        class="lottery-title"
        src="../../../assets/static/lottery-title01.png"
      />
      <div class="lottery-normal">
        <img src="../../../assets/static/lottery-normal.png" class="bg" />
        <div class="balls">
          <Ball class="yellow-ball b1" color="yellow" />
          <Ball class="blue-ball b2" color="blue" />
          <Ball class="purple-ball b3" color="purple" />
          <Ball class="blue-ball b4" color="blue" />

          <Ball class="blue-ball b5" color="blue" />
          <Ball class="blue-ball b6" color="blue" />
          <Ball class="red-ball b7" color="red" />
          <Ball class="purple-ball b8" color="purple" />
          <Ball class="blue-ball b9" color="blue" />

          <Ball class="purple-ball b10" color="purple" />
          <Ball class="yellow-ball b11" color="yellow" />
          <Ball class="blue-ball b12" color="blue" />
        </div>
      </div>
    </div>
    <div class="controller">
      <img src="../../../assets/static/part1.png" class="bg" />
      <div class="btn-group">
        <img src="../../../assets/static/left-left.png" class="left-btn" />
        <div class="start-btn">
          <img src="../../../assets/static/o-btn.png" class="btn-img" />
          <div>
            <div class="btn-text-main">开始抽奖</div>
            <div class="btn-text-coin">
              <img src="../../../assets/static/coin.png" />
            </div>
            X 10
          </div>
        </div>
        <img src="../../../assets/static/left-right.png" class="right-btn" />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Ball from "./ball.vue";
</script>

<style lang="scss" scoped>
$title-z-index: 300;
$balls-z-index: 205;
$lottery-normal-z-index: 200;
$controller-z-index: 100;
$btn-group-z-index: 400;

.page {
}
.star {
  display: flex;
  justify-content: space-between;
}

.machine {
  width: 100%;
  margin-top: -5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  .lottery-title {
    box-sizing: border-box;
    padding: 0 2rem 0 2rem;
    position: relative;
    width: 100%;
    z-index: $title-z-index;
  }
  .lottery-normal {
    position: relative;
    margin-top: -2.8rem;
    width: 100%;
    z-index: $lottery-normal-z-index;
    .bg {
      position: absolute;
      width: 80%;
      left: 0;
      right: 0;
      margin: auto;
    }
    .balls {
      position: absolute;
      width: 100%;
      z-index: $balls-z-index;
      .blue-ball {
        $size: 16vw;
        width: $size;
        height: $size;
      }
      .purple-ball {
        $size: 19vw;
        width: $size;
        height: $size;
      }
      .yellow-ball {
        $size: 22vw;
        width: $size;
        height: $size;
      }
      .red-ball {
        $size: 28vw;
        width: $size;
        height: $size;
      }

      @keyframes b1 {
        from {
          top: 8.5vw;
        }
        to {
          top: 10.5vw;
        }
      }

      .b1 {
        position: absolute;
        left: 14vw;
        animation: b1 1s ease-in-out infinite alternate;
      }

      @keyframes b2 {
        from {
          top: -4vw;
        }
        to {
          top: -2vw;
        }
      }

      .b2 {
        position: absolute;
        left: 32vw;
        animation: b2 1s ease-in-out infinite alternate;
      }

      @keyframes b3 {
        from {
          top: 0vw;
        }
        to {
          top: 2.5vw;
        }
      }

      .b3 {
        position: absolute;
        left: 53vw;
        animation: b3 1s ease-in-out infinite alternate;
      }

      @keyframes b4 {
        from {
          top: 3.5vw;
        }
        to {
          top: 6vw;
        }
      }

      .b4 {
        position: absolute;
        left: 75vw;
        animation: b4 1s ease-in-out infinite alternate;
      }

      @keyframes b5 {
        from {
          top: 34vw;
        }
        to {
          top: 36vw;
        }
      }

      .b5 {
        position: absolute;
        left: 4vw;
        animation: b5 1s ease-in-out infinite alternate;
      }

      @keyframes b6 {
        from {
          top: 30vw;
        }
        to {
          top: 33vw;
        }
      }

      .b6 {
        position: absolute;
        left: 22vw;
        animation: b6 1s ease-in-out infinite alternate;
      }
      @keyframes b7 {
        from {
          top: 22vw;
        }
        to {
          top: 24vw;
        }
      }
      .b7 {
        position: absolute;
        left: 37vw;
        animation: b7 1s ease-in-out infinite alternate;
      }
      @keyframes b8 {
        from {
          top: 26.5vw;
        }
        to {
          top: 29vw;
        }
      }
      .b8 {
        position: absolute;
        left: 65vw;
        animation: b8 1s ease-in-out infinite alternate;
      }
      @keyframes b9 {
        from {
          top: 33vw;
        }
        to {
          top: 38vw;
        }
      }
      .b9 {
        position: absolute;
        left: 83vw;
        animation: b9 1s ease-in-out infinite alternate;
      }
      @keyframes b10 {
        from {
          top: 48vw;
        }
        to {
          top: 51vw;
        }
      }
      .b10 {
        position: absolute;
        left: 22vw;
        animation: b10 1s ease-in-out infinite alternate;
      }
      @keyframes b11 {
        from {
          top: 48vw;
        }
        to {
          top: 53vw;
        }
      }
      .b11 {
        position: absolute;
        left: 45vw;
        animation: b11 1s ease-in-out infinite alternate;
      }
      @keyframes b12 {
        from {
          top: 48vw;
        }
        to {
          top: 53vw;
        }
      }
      .b12 {
        position: absolute;
        left: 70vw;
        animation: b12 1s ease-in-out infinite alternate;
      }
    }
  }
}
.controller {
  width: 100%;
  position: relative;

  margin-top: 68vw;
  .bg {
    z-index: $controller-z-index;
    position: absolute;
    width: 100%;
  }
  .btn-group {
    width: 100%;
    position: relative;
    z-index: $btn-group-z-index;
    .left-btn {
      position: absolute;
      top: 5vw;
      left: 12vw;
      width: 12vw;
    }
    .start-btn {
      position: relative;

      .btn-img {
        position: absolute;
        width: 100%;
        top: 7vw;
        left: 30vw;
        width: 40vw;
      }
      .btn-text-main {
        position: absolute;
        top: 8vw;
        left: 42vw;
        font-size: 18px;
        font-weight: bold;
        color: #75231e;
        letter-spacing: 1.3px;
        -webkit-text-stroke: 0.2px #75231e;
      }
      .btn-text-coin{
        position: absolute;
        top: 12vw;
        left: 42vw;
        width: 1.5rem;
        img{
            width: 100%;
        }
      }
    }
    .right-btn {
      position: absolute;
      top: 5vw;
      left: 77vw;
      width: 12vw;
    }
  }
}
</style>
