<script setup>
import { ref } from 'vue'

let notification = ref(0)
function addValue() {
  notification.value++
  // if(notification.value>100){
  //   notification.value=99+
  // }
}
// function restValue(){
//   if(notification.value<=0){
//     return
//   }
//   notification.value--
//   console.log(notification)
// }
function restValue() {
  if (notification.value > 0) {
    notification.value--
  }
}
</script>

<template>
  <div class="wrapper">
    <div class="profile">
      <div class="globo" v-if="notification > 0">{{ notification }}</div>
    </div>
    <div class="buttom-wrapper">
      <div class="buttom" @click="restValue">-</div>
      <div class="buttom" @click="addValue">+</div>
    </div>
    <div  class="" v-if="notification ==0">eres un casper :v 🍑</div>
    <div class="" v-else>revisa tu inbox mmgvo😴</div>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: #025e73;
  width: 60%;
  border-radius: 8px;
  margin: 0 auto;
  padding-top: 32px;
  overflow: hidden;
}
.profile {
  background-color: blueviolet;
  width: 120px;
  height: 120px;
  border-radius: 100%;
  margin: 0 auto;
  position: relative;
  background-image: url(https://fcb-abj-pre.s3.amazonaws.com/img/jugadors/763_ronaldinho.jpg);
  background-size: cover;
}
.globo {
  position: absolute;
  background-color: #011f26;
  font-weight: bold;
  min-width: 20px;
  height: 20px;
  border-radius: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: wheat;
  top: 10px;
  right: 6px;
}
.buttom-wrapper {
  background-color: #025e73;
  text-align: center;
  margin: 12px;
}
.buttom {
  background-color: #f2a71b;
  border-radius: 5px;
  padding: 2px 0px;
  font-weight: bold;
  color: white;
  display: inline-block;
  cursor: pointer;
  width: 40px;
  /* margin: 0 20px 0 20px; */
}
.buttom:first-child {
  margin-right: 10px;
}
.buttom:last-child {
  margin-left: 8px;
}
</style>
