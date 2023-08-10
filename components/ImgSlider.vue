<template>
  <div class="slider">
    <Splide :options="options" aria-label="My Favorite Images">
      <SplideSlide v-for="(image, index) in images" :key="index">
        <img :src="`/img/${image}`" alt="image" />
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
const images = [
  "0EC74747-7357-472C-AE2B-6148FD5DC204.JPG",
  "1B7A3907-7F00-4F1B-BAD0-452865534B18.JPG",
  "1ECE557A-1129-42D8-9BD6-F3143D51D181.JPG",
  "04A216C2-2CE5-4F4D-AF4B-3F9177DB7963.JPG",
  "4F3C348D-7267-44E2-A879-FE180CEBD098.JPG",
  "9B9B2C76-C965-4B83-B12D-D1ECD5267E1E.JPG",
  "9D261FE2-1391-442E-BC23-D8CFD29A159D.jpg",
  "28A681D3-EA12-4C63-9D5B-372B84CC2270.JPG",
  "8236CA44-2BF2-4CDC-A30E-192C31BAF1DA.jpg",
  "A4483478-0B23-465C-B18E-BD43F462A54A.JPG",
  "E86BB3AF-D263-4341-9C80-615C9D20CC60.JPG",
  "F86E5D4F-B123-4594-9258-A0C19931BDB1.JPG",
  "fe122ae1-0fab-4097-979a-3059c34cf466.jpg",
  "image-removebg-preview.png",
  "IMG_0089.jpeg",
  "IMG_0090.jpeg",
  "IMG_0094.jpeg",
  "IMG_3468.JPG",
  "IMG_3487.JPG",
  "IMG_3511.JPG",
  "IMG_3512.JPG",
  "IMG_3513.JPG",
  "IMG_3515.PNG",
  "IMG_3523.JPG",
  "IMG_3524.JPG",
  "IMG_3525.JPG",
  "IMG_3526.JPG",
  "IMG_3615.JPG",
  "IMG_3623.JPG",
  "IMG_3624.JPG",
  "IMG_3625.JPG",
  "IMG_3631.JPG",
  "IMG_3677.JPG",
  "IMG_3678.JPG",
  "IMG_3679.JPG",
  "IMG_3695.JPG",
  "IMG_3696.JPG",
  "IMG_3697.JPG",
  "IMG_3707.JPG",
  "IMG_3790.JPG",
  "IMG_3948.JPG",
  "IMG_3949.JPG",
  "IMG_3950.JPG",
  "IMG_3951.JPG",
  "IMG_3952.JPG",
  "IMG_3956.PNG",
  "IMG_3967.JPG",
  "IMG_3986.JPG",
  "IMG_3989.PNG",
  "IMG_4323.JPG",
  "IMG_4457.JPG",
  "IMG_4458.JPG",
];
</script>

<style scoped>
.slider {
  width: 80%;
  height: 80%;
  overflow: hidden;
}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>
