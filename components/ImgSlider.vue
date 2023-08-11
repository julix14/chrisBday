<template>
  <div class="slider">
    <Splide :options="options" aria-label="My Favorite Images">
      <SplideSlide v-for="(image, index) in shuffleArray(images)" :key="index">
        <img :src="`/img/${image}`" alt="image" loading="lazy" />
      </SplideSlide>
      <div class="splide__progress">
        <div class="splide__progress__bar"></div>
      </div>
    </Splide>
  </div>
</template>

<script setup>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";

function shuffleArray(array) {
  for (let i = array.length - 1; i > 0; i--) {
    // Generate a random index between 0 and i (inclusive)
    const randomIndex = Math.floor(Math.random() * (i + 1));

    // Swap elements at i and randomIndex
    const temp = array[i];
    array[i] = array[randomIndex];
    array[randomIndex] = temp;
  }
  return array;
}

const options = {
  rewind: true,
  perPage: 2,
  gap: "1rem",
  autoplay: true,

  breakpoints: {
    1000: {
      perPage: 2,
    },
  },
};

// Get an array of all imagenames from the folder "public/img"
const images = [
  "0a412694-e15e-42a3-a5bb-ef1a674bb1a7.JPG",
  "0EC74747-7357-472C-AE2B-6148FD5DC204.JPG",
  "1B7A3907-7F00-4F1B-BAD0-452865534B18.JPG",
  "1e39d97b-c4e8-4b27-94af-e357f134f531.JPG",
  "1ECE557A-1129-42D8-9BD6-F3143D51D181.JPG",
  "04A216C2-2CE5-4F4D-AF4B-3F9177DB7963.JPG",
  "4cd7c05d-9580-4f4e-9e24-33300b606af1.JPG",
  "4F3C348D-7267-44E2-A879-FE180CEBD098.JPG",
  "6fc6021b-ff33-46ea-9c2e-23497716544b.JPG",
  "9B9B2C76-C965-4B83-B12D-D1ECD5267E1E.JPG",
  "9D261FE2-1391-442E-BC23-D8CFD29A159D.jpg",
  "28A681D3-EA12-4C63-9D5B-372B84CC2270.JPG",
  "54b9f5c9-f2cc-49d3-9953-abccb9a321b2.JPG",
  "63aaff18-7bc5-49a2-b790-18a6662e16a7.JPG",
  "74b9ed76-3a5a-42c5-8543-f8e71a50ff79.JPG",
  "0422d364-cd2b-422f-abd1-40e66083beed.JPG",
  "8236CA44-2BF2-4CDC-A30E-192C31BAF1DA.jpg",
  "339028b5-062b-4bfc-b1b9-23763361e116.JPG",
  "438176ad-8cca-4f4d-956f-6bce4d7320da.JPG",
  "63977759-c2e8-449a-a95b-7812a07fd49b.JPG",
  "A4483478-0B23-465C-B18E-BD43F462A54A.JPG",
  "d024a26f-c4cf-45ee-aa01-c6dbef8633b0.JPG",
  "E86BB3AF-D263-4341-9C80-615C9D20CC60.JPG",
  "f12b7d4c-3d08-429c-999e-048a35bd8a08.JPG",
  "f84c2804-3e54-461c-a984-710e3e482e67.JPG",
  "F86E5D4F-B123-4594-9258-A0C19931BDB1.JPG",
  "fe122ae1-0fab-4097-979a-3059c34cf466.jpg",
  "image-removebg-preview.JPG",
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
  "IMG_6938.JPG",
  "IMG_6940.JPG",
  "IMG_6943.JPG",
  "IMG_6944.JPG",
  "IMG_7067.JPG",
  "IMG_7073.JPG",
  "IMG_7077.JPG",
  "IMG_7085.JPG",
  "IMG_7145.JPG",
  "IMG_7251.JPG",
  "IMG_7288.JPG",
  "IMG_7290.JPG",
  "IMG_7308.JPG",
  "IMG_7309.JPG",
  "IMG_7388.JPG",
  "WhatsApp Image 2023-08-10 at 22.43.52.jpeg",
];
</script>

<style scoped>
.slider {
  width: 1000px;
  height: 500px;
  overflow: hidden;
}

img {
  width: 450px;
  height: 500px;
  object-fit: contain;
}
</style>
