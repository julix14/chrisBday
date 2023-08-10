<template>
  <div class="slider">
    <Splide :options="options" aria-label="My Favorite Images">
      <SplideSlide>
        <img
          src="img/0EC74747-7357-472C-AE2B-6148FD5DC204.JPG"
          alt="Sample 1"
        />
      </SplideSlide>
      <SplideSlide>
        <img
          src="img/0EC74747-7357-472C-AE2B-6148FD5DC204.JPG"
          alt="Sample 2"
        />
      </SplideSlide>
    </Splide>
  </div>
</template>

<script setup>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";

const options = {
  rewind: true,
  perPage: 2,
  gap: "1rem",
  breakpoints: {
    1000: {
      perPage: 1,
    },
  },
};

// Get an array of all imagenames from the folder "public/img"
const images = require.context("../public/img", false, /\.jpg$/);
</script>

<style scoped>
.slider {
  width: 80vh;
  height: 80vh;
  overflow: hidden;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
