<template>
  <div class="page">
    <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/daybg.png" class="bg-img" />
    <div class="content">
      <div class="flex-box">
        <div class="text">
          <div class="line1">
            <div>每日登录</div>
            <div>+1个</div>
          </div>
          <div class="line2">
            <div>每日登录可获得一个神灯币</div>
            <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/coin.png" />
          </div>
        </div>
        <div class="r-btn" @click="onLogin">{{ status }}</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { Toast } from "vant";
import { ref } from "vue";
let status = ref<string>("领取");

function onLogin() {
  Toast.loading({
    message: "登录中...",
    forbidClick: true,
    duration: 1500,
  });
  setTimeout(() => {
    status.value = "已领取";
  }, 1500);
}
</script>

<style lang="scss" scoped>
.page {
  position: relative;
  .bg-img {
    position: absolute;
    width: 100%;
    top: 0;
  }

  .content {
    position: absolute;
    width: 100%;
    top: 0;
    .flex-box {
      display: flex;
      width: 100%;
      justify-content: space-around;
      .text {
        display: flex;
        flex-direction: column;
        @media screen and (min-width: 375px) {
          margin-top: 5vw;
        }
        @media screen and (min-width: 500px) {
          margin-top: 6.5vw;
        }
        gap: 1vw;
        .line1 {
          display: flex;
          align-items: center;
          div:nth-child(1) {
            color: #342656;
            font-size: 22px;
            font-weight: bolder;
            -webkit-text-stroke: 0.4px #342656;
            margin-right: 1.5vw;
          }
          div:nth-child(2) {
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            background: #f2933e;
            width: 10vw;
            font-size: 14px;
            font-weight: bolder;
            height: 4.5vw;
            border-radius: 1vw;
          }
          @media screen and (min-width: 375px) {
            div:nth-child(1) {
              font-size: 16px;
              -webkit-text-stroke: 0.4px #342656;
              margin-right: 1.5vw;
            }
            div:nth-child(2) {
              font-size: 12px;
            }
          }
          @media screen and (min-width: 620px) {
            div:nth-child(1) {
              font-size: 22px;
              -webkit-text-stroke: 0.4px #342656;
              margin-right: 1.5vw;
            }
            div:nth-child(2) {
              font-size: 14px;
            }
          }
          @media screen and (min-width: 680px) {
            div:nth-child(1) {
              font-size: 28px;
              -webkit-text-stroke: 0.4px #342656;
              margin-right: 1.5vw;
            }
            div:nth-child(2) {
              font-size: 18px;
            }
          }
          @media screen and (min-width: 880px) {
            div:nth-child(1) {
              font-size: 34px;
              -webkit-text-stroke: 0.4px #342656;
              margin-right: 1.5vw;
            }
            div:nth-child(2) {
              font-size: 20px;
            }
          }
          @media screen and (min-width: 1160px) {
            div:nth-child(1) {
              font-size: 38px;
              -webkit-text-stroke: 0.4px #342656;
              margin-right: 1.5vw;
            }
            div:nth-child(2) {
              font-size: 26px;
            }
          }
        }
        .line2 {
          display: flex;
          align-items: center;
          color: #6a49a5;
          font-size: 14px;
          font-weight: bold;
          img {
            width: 5vw;
          }
          @media screen and (min-width: 375px) {
            font-size: 12px;
          }
          @media screen and (min-width: 620px) {
            font-size: 18px;
          }
          @media screen and (min-width: 680px) {
            font-size: 20px;
          }
          @media screen and (min-width: 880px) {
            font-size: 22px;
          }
          @media screen and (min-width: 1160px) {
            font-size: 24px;
          }
        }
      }
      .r-btn {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 27vw;
        height: 9vw;
        overflow: hidden;
        margin-top: 7vw;
        background: url("../../../assets/static/r-btn.png");
        background-size: 100%;
        font-size: 20px;
        color: #fff;
        letter-spacing: 3px;
        -webkit-text-stroke: #fff 0.4px;
        @media screen and (min-width: 375px) {
          font-size: 18px;
        }
        @media screen and (min-width: 620px) {
          font-size: 22px;
        }
        @media screen and (min-width: 680px) {
          font-size: 26px;
          -webkit-text-stroke: #fff 0.6px;
        }
        @media screen and (min-width: 880px) {
          font-size: 32px;
          -webkit-text-stroke: #fff 0.8px;
        }
        @media screen and (min-width: 1160px) {
          font-size: 44px;
          -webkit-text-stroke: #fff 1.5px;
        }
      }
    }
  }
}
</style>
