<template>
  <div class="md:hidden">
    <Swiper
      :modules="[SwiperAutoplay]"
      :slides-per-view="1"
      :loop="true"
      :autoplay="{
        delay: 2000,
        disableOnInteraction: true,
      }"
    >
      <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
        <div
          class="w-72 bg-white shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl"
        >
          <img
            :src="slide.url"
            alt="Product"
            class="h-80 w-72 object-cover rounded-t-xl"
          />
          <div class="px-4 py-3 w-72 flex flex-col items-center">
            <p class="text-lg font-serif text-red-500 block capitalize">
              {{ slide.title }}
            </p>
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </div>
  <div class="hidden md:block">
    <Swiper
      :modules="[SwiperAutoplay]"
      :slides-per-view="3"
      :loop="true"
      :autoplay="{
        delay: 2000,
        disableOnInteraction: true,
      }"
    >
      <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
        <div
          class="w-72 bg-white shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl"
        >
          <img
            :src="slide.url"
            alt="Product"
            class="h-80 w-72 object-cover rounded-t-xl"
          />
          <div class="px-4 py-3 w-72 flex flex-col items-center">
            <p class="text-lg font-serif text-red-500 block capitalize">
              {{ slide.title }}
            </p>
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </div>
</template>
<script setup>
const slides = [
  {
    url: "/fame4.png",
    title: "Each One, Adapt One",
    content: "",
  },
  {
    url: "/fame5.png",
    title: "Let's Leave No Child Uneducated",
    content: "",
  },
  {
    url: "/fame6.png",
    title: "Waste to Wonder: Transforming Trash into Treasures",
    content: "",
  },
];
</script>
<style scoped>
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  height: 70vh;
  margin: 2px;
  font-size: 4rem;
  font-weight: bold;
  font-family: "Roboto", sans-serif;
}
.swiper-wrapper {
  min-width: 100vh;
  width: 100vh;
}
.swiper-cards {
  width: 240px;
  height: 240px;
}
.swiper-cards .swiper-slide {
  border-radius: 6px;
  border: 1px solid black;
}
</style>
