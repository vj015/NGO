<template>
  <div>
    <Swiper
      :modules="[SwiperAutoplay]"
      :slides-per-view="screenVal"
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
            alt="Campaign"
            class="h-80 w-72 object-cover rounded-t-xl"
          />
          <div
            class="px-4 py-3 w-72 flex flex-col items-center"
            v-if="from === 'projects'"
          >
            <p
              class="text-xl mb-2 text-center font-semibold font-serif text-red-500 block capitalize"
            >
              {{ slide.title }}
            </p>
            <button
              href="#"
              class="w-auto px-4 py-2 m-2 text-red-500 rounded font-mono text-xl border-2 border-red-500 hover:text-white hover:bg-red-500"
            >
              Explore
              <span class="inline-block align-middle"><IconsRightarrow /></span>
            </button>
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </div>
</template>
<script setup>
import { toRefs } from "vue";

let props = defineProps(["screenVal", "slides", "from"]);
const { screenVal } = toRefs(props);
</script>
<style>
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
}
.swiper-wrapper {
  padding: 15px 0 !important;
}
</style>
