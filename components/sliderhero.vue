<template>
  <Swiper
    :modules="[SwiperAutoplay, SwiperNavigation, SwiperPagination]"
    :slides-per-view="1"
    :loop="true"
    :navigation="true"
    :pagination="true"
    :autoplay="{
      delay: 8000,
      disableOnInteraction: true,
    }"
  >
    <SwiperSlide
      v-for="(slide, idx) in slides"
      :key="idx"
      :style="{ backgroundImage: `url(${slide.url})` }"
      class="bg-center bg-fixed bg-cover bg-no-repeat customh min-w-screen bg-opacity-50 font-extrabold leading-tight text-9xl text-white underline flex flex-col"
    >
      <div>{{ slide.quote }}</div>
      <div>
        <button
          @click="navigateTo('/about')"
          class="w-auto px-4 py-2 mt-3 sha text-center text-white bg-red-500 rounded text-xl border-2 border-red-500 hover:text-red-500 hover:bg-white"
        >
          Explore
          <span class="inline-block align-middle"><rightarrow /></span>
        </button>
      </div>
    </SwiperSlide>
  </Swiper>
</template>
<script setup>
import rightarrow from "/components/icons/rightarrow.vue";
const slides = [
  {
    url: "/BG/dummy.webp",
    quote: "Help Us Give a Voice to Every Child in Need",
  },
  {
    url: "/BG/BG-1.webp",
    quote: "Join Hands with Us to Give Every Child a Better Tomorrow",
  },
  {
    url: "/BG/BG-2.webp",
    quote: "Empowering Children to Reach Their Full Potential",
  },
  {
    url: "/BG/BG-3.webp",
    quote: "Together, Lets make a better world!",
  },
  {
    url: "/BG/BG-4.webp",
    quote:
      "Building a Brighter Future for Every Child: Join Us on the Journey!",
  },
];
</script>
<style scoped>
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 40px;
  text-align: center;
  padding: 0 40px;
  font-family: "Spectral", serif;
  text-shadow: 2px 2px #ff0000;
}
.swiper-wrapper {
  min-width: 100vh;
  width: 100vh;
}
.swiper-cards .swiper-slide {
  border-radius: 6px;
  border: 1px solid black;
}

.swiper-cards {
  width: 80%;
  height: 90%;
}
.swiper-button-next,
.swiper-button-prev {
  color: white !important;
}
.swiper-pagination-bullet-active {
  background-color: white !important;
}
.customh {
  height: 87vh;
}
.sha {
  text-shadow: 2px 2px #ff0000;
}
</style>
