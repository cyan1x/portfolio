<script setup lang="ts">
import { ref } from 'vue';

const amount = 14
const sizes = [...Array(amount)].map(() => randomInt(8, 16))
const lefts = [...Array(amount)].map(() => randomInt(1, 99))

function randomInt(min: number, max: number) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
</script>

<template>
  <ul class="background">
    <slot></slot>
    <li v-for="size, index in sizes" class="absolute block list-none bg-slate-500 animate-[animate_5s_linear_infinite]"
      :class="[`size-12`, `bottom-12`, `left-12`]"></li>
    <!-- <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li> -->
  </ul>
</template>

<style scoped>
@keyframes animate {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 1;
    border-radius: 0;
  }

  100% {
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
    border-radius: 50%;
  }
}

.background {
  position: relative;
  max-width: 100vw;
  height: 100%;
  top: 0;
  left: 0;
  margin: 0;
  padding: 0;
  background: #f2f4f5;
  background-attachment: local;
  overflow: hidden;
  overflow-x: hidden;
}

/* .background li {
  position: absolute;
  display: block;
  list-style: none;
  width: 20px;
  height: 20px;
  background: rgba(203, 203, 203, 0.25);
  animation: animate 5s linear infinite;
} */

/* .background li:nth-child(0) {
  left: 80%;
  width: 75px;
  height: 75px;
  bottom: -75px;
  animation-delay: 1s;
}

.background li:nth-child(1) {
  left: 51%;
  width: 118px;
  height: 118px;
  bottom: -118px;
  animation-delay: 2s;
}

.background li:nth-child(2) {
  left: 9%;
  width: 103px;
  height: 103px;
  bottom: -103px;
  animation-delay: 6s;
}

.background li:nth-child(3) {
  left: 37%;
  width: 121px;
  height: 121px;
  bottom: -121px;
  animation-delay: 12s;
}

.background li:nth-child(4) {
  left: 53%;
  width: 178px;
  height: 178px;
  bottom: -178px;
  animation-delay: 17s;
}

.background li:nth-child(5) {
  left: 27%;
  width: 75px;
  height: 75px;
  bottom: -75px;
  animation-delay: 24s;
}

.background li:nth-child(6) {
  left: 36%;
  width: 143px;
  height: 143px;
  bottom: -143px;
  animation-delay: 6s;
}

.background li:nth-child(7) {
  left: 38%;
  width: 141px;
  height: 141px;
  bottom: -141px;
  animation-delay: 6s;
}

.background li:nth-child(8) {
  left: 10%;
  width: 123px;
  height: 123px;
  bottom: -123px;
  animation-delay: 9s;
}

.background li:nth-child(9) {
  left: 71%;
  width: 119px;
  height: 119px;
  bottom: -119px;
  animation-delay: 18s;
}

.background li:nth-child(10) {
  left: 50%;
  width: 126px;
  height: 126px;
  bottom: -126px;
  animation-delay: 39s;
}

.background li:nth-child(11) {
  left: 32%;
  width: 118px;
  height: 118px;
  bottom: -118px;
  animation-delay: 1s;
}

.background li:nth-child(12) {
  left: 43%;
  width: 138px;
  height: 138px;
  bottom: -138px;
  animation-delay: 12s;
}

.background li:nth-child(13) {
  left: 61%;
  width: 165px;
  height: 165px;
  bottom: -165px;
  animation-delay: 40s;
}

.background li:nth-child(14) {
  left: 71%;
  width: 117px;
  height: 117px;
  bottom: -117px;
  animation-delay: 31s;
} */
</style>