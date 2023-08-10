<template>
  <div class="container" @click="playAudio()">
    <ConfettiExplosion
      :particleCount="900"
      :force="0.7"
      :duration="5000"
      :shouldDestroyAfterDone="false"
    />
    <p class="happyBDay">Happy Birthday!!!</p>
    <ImgSlider />
  </div>
</template>

<script setup>
// import function to register Swiper custom elements
import ImgSlider from "@/components/ImgSlider.vue";
import ConfettiExplosion from "vue-confetti-explosion";
import "regenerator-runtime/runtime";

console.log("playing");

function playAudio() {
  const audio = new Audio("/sounds/happyBirthday.mp3");

  audio.play();
  console.log("playing");
}
</script>

<style scoped>
.happyBDay {
  font-size: 7.5rem;
  font-weight: bold;
  font-family: Arial, Helvetica, sans-serif;
  text-decoration: underline;
  background-image: linear-gradient(
    50deg,
    #ca4246 16.666%,
    #e16541 16.666%,
    #e16541 33.333%,
    #f18f43 33.333%,
    #f18f43 50%,
    #8b9862 50%,
    #8b9862 66.666%,
    #476098 66.666%,
    #476098 83.333%,
    #a7489b 83.333%
  );
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  margin-bottom: 1rem;
}
.container {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

* {
  margin: 0;
  overflow: hidden;
}
</style>
