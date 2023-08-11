<template>
  <main class="main">
    <h1 class="colored-heading">{{showPictures ? "Happy Birthday!!!" : "We want to celebrate your birthday with you today!" }}</h1>

    <div v-if="showPictures" class="confetti-container">
      <ConfettiExplosion
        :particleCount="900"
        :force="0.7"
        :duration="5000"
        :shouldDestroyAfterDone="true"
      />
    </div>
    <ImgSlider v-if="showPictures" />

    <button v-else="showPictures" @click="hideModal()" class="orange-button">Continue to your party!</button>
  </main>
</template>

<script setup>
import ImgSlider from "@/components/ImgSlider.vue";
import ConfettiExplosion from "vue-confetti-explosion";
import "regenerator-runtime/runtime";

const showPictures = ref(false);

function hideModal() {
  const audio = new Audio("/sounds/happyBirthday.mp3");
  audio.play();

  showPictures.value = true;
}
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  gap: 4rem;
  padding: 4rem;
  font-family: Arial, Helvetica, sans-serif;
  box-sizing: border-box;
}

.colored-heading {
  font-size: 4rem;
  text-align: center;
  font-weight: bold;
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
}

.orange-button {
  all: unset;
  padding: 1rem 2rem;
  border-radius: 5px;
  background-color: #e16541;
  color: white;
  cursor: pointer;
}
.orange-button:hover {
  opacity: 0.9;
}

.confetti-container {
  position: absolute;
  inset: auto;
  top: 0;
  height: 10vh;
  z-index: 100;
  background-color: #476098;
}

@media (max-width: 768px) {
  .main {
    padding: 2rem;
    gap: 2rem;
  }
  .colored-heading {
    font-size: 2rem;
  }
}
</style>

<style>
* {
  margin: 0;
}
</style>
