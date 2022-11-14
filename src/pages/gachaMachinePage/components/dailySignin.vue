<template>
  <div class="page">
    <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/part2.png" class="bg" />
    <div class="content">
      <div class="flex-box1">
        <div class="item" v-for="i in obj1" key="i" @click="signin(i)">
          第{{
            i.index == 1 ? "一" : i.index == 2 ? "二" : i.index == 3 ? "三" : i.index == 4 ? "四" : ""
          }}天
          <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/icon-gift.png" />
          <div>{{i.status?'已领取':'签到领取'}}</div>
        </div>
      </div>
      <div class="flex-box2">
        <div class="item1" v-for="i of obj2" key="i" @click="signin(i)">
          第{{ i.index == 1 ? "五" : "六" }}天
          <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/icon-gift.png" />
          <div>{{i.status?'已领取':'签到领取'}}</div>
        </div>
        <div class="item2" @click="signin(obj3[0])">
          <div class="flex-box">
            第七天
            <img src="https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/box-chose21.png" />
          </div>
          <div>{{obj3[0].status?'已领取':'签到领取'}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { Toast } from "vant";
import {ref} from 'vue'
let obj1 = ref([{status:0,index:1},{status:0,index:2},{status:0,index:3},{status:0,index:4}])
let obj2 = ref([{status:0,index:5},{status:0,index:6}])
let obj3 = ref([{status:0,index:7}])

function signin(row:any){
  console.log(row)
  row.status = 1;
  Toast.success('签到成功')
}

</script>

<style lang="scss" scoped>
.page {
  position: relative;
  .bg {
    position: absolute;
    width: 100%;
  }
  .content {
    position: absolute;
    width: 100%;
    top: 13vw;
    .flex-box1 {
      display: flex;
      flex-wrap: wrap;
      padding: 0 9vw 0 9vw;
      justify-content: space-between;
      .item {
        display: flex;
        flex-direction: column;
        font-weight: bold;
        align-items: center;
        justify-content: center;
        background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/s1.png");
        background-size: 100%;
        background-repeat: no-repeat;
        width: 17vw;
        height: 16.5vw;
        img {
          width: 10vw;
        }
        font-size: 12px;
        line-height: 20px;
        div {
          background: #5ed2ee;
          width: 17vw;
          text-align: center;
          line-height: 16px;
          border-radius: 0 0 1.5vw 1.5vw;
          margin-top: -1vw;
          color: #222a5a;
        }
        @media screen and (min-width: 620px) {
          font-size: 15px;
          div {
            line-height: 24px;
          }
        }
        @media screen and (min-width: 680px) {
          font-size: 18px;
          div {
            line-height: 30px;
          }
        }
        @media screen and (min-width: 880px) {
          font-size: 22px;
          div {
            line-height: 35px;
          }
        }
        @media screen and (min-width: 1160px) {
          font-size: 28px;
          div {
            line-height: 70px;
          }
        }
      }
    }
    .flex-box2 {
      display: flex;
      flex-wrap: wrap;
      padding: 0 9vw 0 9vw;
      justify-content: space-between;
      margin-top: 4vw;
      .item1 {
        display: flex;
        flex-direction: column;
        font-weight: bold;
        align-items: center;
        justify-content: center;
        background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/s1.png");
        background-size: 100%;
        background-repeat: no-repeat;
        width: 22vw;
        height: 16.5vw;
        border-radius: 1.5vw;
        img {
          width: 10vw;
        }
        font-size: 12px;
        line-height: 20px;
        div {
          background: #5ed2ee;
          width: 22vw;
          text-align: center;
          line-height: 16px;
          border-radius: 0 0 1.5vw 1.5vw;
          margin-top: -1vw;
          color: #222a5a;
        }
        @media screen and (min-width: 620px) {
          font-size: 15px;
          div {
            line-height: 24px;
          }
        }
        @media screen and (min-width: 680px) {
          font-size: 18px;
          div {
            line-height: 30px;
          }
        }
        @media screen and (min-width: 880px) {
          font-size: 22px;
          div {
            line-height: 35px;
          }
        }
        @media screen and (min-width: 1160px) {
          font-size: 28px;
          div {
            line-height: 70px;
          }
        }
      }
      .item2 {
        display: flex;
        flex-direction: column;
        font-weight: bold;
        align-items: center;
        justify-content: center;
        background: url("https://vichien-public.oss-cn-guangzhou.aliyuncs.com/gachaMachine/s3.png");
        background-size: 100% 100%;
        background-repeat: no-repeat;
        width: 30vw;
        height: 16.5vw;
        border-radius: 1.5vw;
        .flex-box {
          display: flex;
          justify-content: space-around;
          align-items: center;
          font-size: 16px;

          img {
            width: 13vw;
          }
        }
        font-size: 12px;
        line-height: 20px;
        div:nth-child(2) {
          background: rgb(242, 175, 89);
          background: linear-gradient(
            90deg,
            rgba(242, 175, 89, 1) 0%,
            rgba(248, 226, 184, 1) 50%,
            rgba(236, 173, 74, 1) 100%
          );
          width: 30vw;
          text-align: center;
          line-height: 16px;
          border-radius: 0 0 1.5vw 1.5vw;
          margin-top: -1vw;
          color: #222a5a;
        }
        @media screen and (min-width: 620px) {
          font-size: 15px;
          .flex-box {font-size: 18px;}
          div:nth-child(2) {
            line-height: 24px;
          }
        }
        @media screen and (min-width: 680px) {
          font-size: 18px;
          .flex-box {font-size: 20px;}
          div:nth-child(2) {
            line-height: 30px;
          }
        }
        @media screen and (min-width: 880px) {
          font-size: 22px;
          .flex-box {font-size: 23px;}
          div:nth-child(2) {
            line-height: 35px;
          }
        }
        @media screen and (min-width: 1160px) {
          font-size: 28px;
          .flex-box {font-size: 30px;}
          div:nth-child(2) {
            line-height: 70px;
          }
        }
      }
    }
  }
}
</style>
