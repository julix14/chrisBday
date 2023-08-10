<template>
  <div class="container">
    <p>Happy Birthday!!!</p>
    <ImgSlider />
  </div>
</template>

<script setup>
// import function to register Swiper custom elements
import ImgSlider from "@/components/ImgSlider.vue";
</script>

<style scoped>
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
