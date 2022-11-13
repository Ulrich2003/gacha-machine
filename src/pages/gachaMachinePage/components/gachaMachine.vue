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
      <!-- 按钮组 -->
      <div class="btn-group">
        <img src="../../../assets/static/left-left.png" class="left-btn" />
        <div class="start-btn">
          <img src="../../../assets/static/o-btn.png" class="btn-img" />
          <div>
            <div class="btn-text-main">开始抽奖</div>
            <div class="btn-text-coin">
              <div>
                <img src="../../../assets/static/coin.png" />
                <text>X 10</text>
              </div>
            </div>
          </div>
        </div>
        <img src="../../../assets/static/left-right.png" class="right-btn" />
      </div>
      <!-- 横条 -->
      <div class="tipbg">
        <img src="../../../assets/static/tipbg.png" />
        <text>左右按键切换奖池</text>
      </div>
      <!-- 底座 -->
      <div class="foundation">
        <img src="../../../assets/static/detialbg.png" class="detialbg" />
        <div class="h-btn">
          <img src="../../../assets/static/h-btn.png" />
          <text>累计奖励</text>
        </div>
        <div class="numbg">
          <img src="../../../assets/static/numbg.png" />
          <div class="text-box">
            <div class="title">剩余XX数量</div>
            <div class="content">1000</div>
          </div>
        </div>
        <img src="../../../assets/static/exit.png" class="exitbg" />
      </div>
    </div>
    <!-- 每日登录 -->
    <daily-login class="daily-login" />
    <!-- 每日签到 -->
    <daily-signin class="daily-signin" />
    <!-- 礼包购买 -->
    <gift-pack-list class="gift-pack-list" />
  </div>
</template>

<script lang="ts" setup>
import Ball from "./ball.vue";
import dailyLogin from "./dailyLogin.vue";
import dailySignin from "./dailySignin.vue";
import giftPackList from "./giftPackList.vue";
</script>

<style lang="scss" scoped>
$controller-z-index: 100;
$lottery-normal-z-index: 200;
$balls-z-index: 205;
$title-z-index: 300;
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
  // 背景图
  .bg {
    z-index: $controller-z-index;
    position: absolute;
    width: 100%;
  }
  // 按钮组
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
        left: 0;
        right: 0;
        text-align: center;
        font-size: 18px;
        font-weight: bold;
        color: #75231e;
        letter-spacing: 1.3px;
        -webkit-text-stroke: 0.2px #75231e;
      }
      @media screen and (min-width: 375px) {
        .btn-text-main {
          font-size: 16px;
          top: 7.7vw;
        }
      }
      @media screen and (min-width: 500px) {
        .btn-text-main {
          font-size: 20px;
          top: 7.8vw;
        }
      }
      @media screen and (min-width: 600px) {
        .btn-text-main {
          font-size: 22px;
          top: 9vw;
        }
      }
      @media screen and (min-width: 1000px) {
        .btn-text-main {
          font-size: 28px;
          top: 9vw;
        }
      }
      @media screen and (min-width: 1160px) {
        .btn-text-main {
          font-size: 46px;
          top: 9.5vw;
        }
      }

      .btn-text-coin {
        position: absolute;
        top: 12.5vw;
        left: 0;
        right: 0;
        width: 100%;
        text-align: center;
        div {
          display: flex;
          justify-content: center;
          align-items: center;
          img {
            width: 3%;
            margin-right: 1%;
          }
          text {
            color: #fefb93;
            font-size: 14px;
          }
          @media screen and (min-width: 375px) {
            text {
              font-size: 12px;
            }
          }
          @media screen and (min-width: 660px) {
            text {
              font-size: 22px;
            }
          }
          @media screen and (min-width: 1160px) {
            text {
              font-size: 46px;
            }
          }
        }
      }
      @media screen and (min-width: 1160px) {
        .btn-text-coin {
          top: 13vw;
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
  // 提示横条
  .tipbg {
    position: relative;
    z-index: $btn-group-z-index;
    width: 100%;
    top: 23vw;
    img {
      position: absolute;
      left: 0;
      right: 0;
      margin: auto;
      width: 90%;
      z-index: 100;
    }
    text {
      width: 100%;
      text-align: center;
      position: absolute;
      z-index: 200;
      font-size: 14px;
      top: 0.3vw;
    }
    @media screen and (min-width: 375px) {
      text {
        font-size: 12px;
        top: -0.6vw;
      }
    }
    @media screen and (min-width: 490px) {
      text {
        font-size: 12px;
        top: 0vw;
      }
    }
    @media screen and (min-width: 620px) {
      text {
        font-size: 19px;
        top: 1vw;
      }
    }
    @media screen and (min-width: 900px) {
      text {
        font-size: 19px;
        top: 1.2vw;
      }
    }
    @media screen and (min-width: 1160px) {
      text {
        font-size: 28px;
        top: 1.7vw;
      }
    }
  }
  // 底座
  .foundation {
    position: relative;
    z-index: $btn-group-z-index;
    width: 100%;
    .detialbg {
      width: 90%;
      position: absolute;
      left: 0;
      right: 0;
      margin: auto;
      top: 32vw;
    }
    .h-btn {
      position: relative;
      width: 20%;
      top: 33vw;
      left: 13vw;
      img {
        position: absolute;
        width: 100%;
        z-index: 100;
      }
      text {
        position: absolute;
        width: 100%;
        z-index: 200;
        text-align: center;
        font-size: 18px;
        top: 2vw;
        font-weight: bolder;
        background-image: linear-gradient(
          180deg,
          rgba(114, 34, 28, 1) 0%,
          rgba(146, 66, 46, 1) 100%
        );
        -webkit-background-clip: text;
        color: transparent;
      }
      @media screen and (min-width: 375px) {
        text {
          font-size: 13px;
          top: 1.5vw;
        }
      }
      @media screen and (min-width: 490px) {
        text {
          font-size: 16px;
          top: 2vw;
        }
      }
      @media screen and (min-width: 620px) {
        text {
          font-size: 22px;
          top: 2.5vw;
        }
      }
      @media screen and (min-width: 880px) {
        text {
          font-size: 25px;
          top: 2.8vw;
        }
      }
      @media screen and (min-width: 1160px) {
        text {
          font-size: 35px;
          line-height: 35px;
          top: 3vw;
        }
      }
    }
    .numbg {
      position: relative;
      left: 38vw;
      top: 33vw;
      width: 30%;
      img {
        position: absolute;
        width: 100%;
        z-index: 100;
      }
      .text-box {
        position: absolute;
        z-index: 200;
        width: 100%;
        text-align: center;
        .title {
          font-weight: bold;
          color: #c1abf2;
          margin-top: 2.8vw;
          line-height: 0px;
        }
        .content {
          color: #f2b569;
          font-size: 20px;
          -webkit-text-stroke: 0.3px #f2b569;
          margin-top: 4.4vw;
          line-height: 0px;
        }
        @media screen and (min-width: 375px) {
          .title {
            font-size: 12px;
            top: 2.5vw;
          }
          .content {
            font-size: 16px;
            -webkit-text-stroke: 0.3px #f2b569;
            top: 2.5vw;
          }
        }
        @media screen and (min-width: 490px) {
          .title {
            font-size: 16px;
            top: 2.5vw;
          }
          .content {
            font-size: 18px;
            -webkit-text-stroke: 0.3px #f2b569;
            top: 2.5vw;
          }
        }
        @media screen and (min-width: 620px) {
          .title {
            font-size: 22px;
            top: 2.5vw;
          }
          .content {
            font-size: 22px;
            -webkit-text-stroke: 0.3px #f2b569;
            top: 2.5vw;
          }
        }
        @media screen and (min-width: 880px) {
          .title {
            font-size: 22px;
            top: 2.5vw;
          }
          .content {
            font-size: 30px;
            -webkit-text-stroke: 0.3px #f2b569;
            top: 2.5vw;
          }
        }
        @media screen and (min-width: 1160px) {
          .title {
            font-size: 25px;
            top: 2.5vw;
          }
          .content {
            font-size: 34px;
            -webkit-text-stroke: 0.3px #f2b569;
            top: 2.5vw;
          }
        }
      }
    }
    .exitbg {
      position: absolute;
      top: 30vw;
      right: 13vw;
      width: 14%;
    }
  }
}

.daily-login {
  position: relative;
  z-index: $controller-z-index;
  width: 97%;
  left: 0;
  right: 0;
  margin: auto;
  top: 48vw;
}

.daily-signin {
  position: relative;
  z-index: $controller-z-index;
  width: 97%;
  left: 0;
  right: 0;
  margin: auto;
  top: 78vw;
}

.gift-pack-list {
  position: relative;
  z-index: $controller-z-index;
  width: 96%;
  left: 0;
  right: 0;
  margin: auto;
  top: 140vw;
}
</style>
