<template>
  <div class="page">
    <img src="../../../assets/static/p3.png" class="bg" />
    <div class="content">
      <div class="item" v-for="i in 5" key="i">
        <div class="relative-box">
          <div>礼包名称礼包名称</div>
          <div>限购0/81</div>
        </div>
        <div class="flex-box">
          <div class="coin" v-for="i in 3">
            <div>
              <img src="../../../assets/static/coin.png" />
              <text>10</text>
            </div>
          </div>
          <div class="r-btn">¥6</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.page {
  position: relative;
  .bg {
    position: absolute;
    width: 100%;
    z-index: 100;
  }
  .content {
    position: relative;
    width: 100%;
    z-index: 200;
    padding: 0 5vw 0 5vw;
    box-sizing: border-box;
    top: 13vw;
    .item {
      background: url("../../../assets/static/item-bg.jpg");
      background-size: 100%;
      width: 100%;
      height: 22.8vw;
      border-radius: 2vw;
      margin-bottom: 5vw;
      .relative-box {
        position: relative;
        font-size: 14px;
        div:nth-child(1) {
          position: absolute;
          top: 1.2vw;
          left: 1vw;
        }
        div:nth-child(2) {
          position: absolute;
          top: 0;
          right: 11.5vw;
          top: 2.2vw;
          font-weight: bold;
        }
        @media screen and (min-width: 375px) {
          font-size: 10px;
          div:nth-child(1) {
            top: 0.35vw;
          }
          div:nth-child(2) {
            top: 1.3vw;
          }
        }
        @media screen and (min-width: 490px) {
          font-size: 14px;
          div:nth-child(1) {
            top: 1vw;
          }
          div:nth-child(2) {
            top: 2vw;
          }
        }
        @media screen and (min-width: 620px) {
          font-size: 16px;
          div:nth-child(1) {
            top: 2.2vw;
          }
          div:nth-child(2) {
            top: 3.2vw;
          }
        }
        @media screen and (min-width: 680px) {
          font-size: 18px;
          div:nth-child(1) {
            left: 2.2vw;
          }
          div:nth-child(2) {
            right: 13.2vw;
          }
        }
        @media screen and (min-width: 880px) {
          font-size: 20px;
          div:nth-child(1) {
            top: 2.5vw;
          }
          div:nth-child(2) {
            top: 3.4vw;
            right: 14vw;
          }
        }
        @media screen and (min-width: 1160px) {
          font-size: 30px;
          div:nth-child(1) {
            top: 2.8vw;
          }
          div:nth-child(2) {
            top: 3.8vw;
            right: 13.5vw;
          }
        }
      }
      .flex-box {
        margin-left: 2vw;
        padding-top: 9vw;
        display: flex;
        align-items: center;
        gap: 3vw;
        .coin {
          background: url("../../../assets/static/i-bg.png");
          background-size: 100%;
          width: 11vw;
          height: 11vw;
          div {
            position: relative;
            img {
              position: absolute;
              top: 1.3vw;
              left: 0;
              right: 0;
              margin: auto;
              width: 80%;
            }
            text {
              font-size: 12px;
              font-weight: bold;
              -webkit-text-stroke: black 0.3px;
              position: absolute;
              top: 7vw;
              right: 0.4vw;
              @media screen and (min-width: 620px) {
                font-size: 14px;
                -webkit-text-stroke: black 0.3px;
              }
              @media screen and (min-width: 680px) {
                top: 7.4vw;

                font-size: 16px;
                -webkit-text-stroke: black 0.3px;
              }
              @media screen and (min-width: 880px) {
                top: 7.8vw;
                font-size: 18px;
                -webkit-text-stroke: black 0.3px;
              }
              @media screen and (min-width: 1160px) {
                top: 8.5vw;
                font-size: 25px;
                -webkit-text-stroke: black 0.3px;
              }
            }
          }
        }
        .r-btn {
          margin-left: 10vw;
          display: flex;
          justify-content: center;
          align-items: center;
          width: 27vw;
          height: 9vw;
          overflow: hidden;
          background: url("../../../assets/static/r-btn.png");
          background-size: 100%;
          font-size: 20px;
          color: #fff;
          letter-spacing: 3px;
          -webkit-text-stroke: #fff 1px;
          @media screen and (min-width: 375px) {
            font-size: 18px;
          }
          @media screen and (min-width: 490px) {
            font-size: 20px;
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
}
</style>
