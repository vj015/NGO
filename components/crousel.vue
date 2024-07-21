<template>
  <div>
    <Swiper
      :modules="[SwiperAutoplay, SwiperNavigation]"
      :slides-per-view="screenVal"
      :loop="!fromTeam"
      :navigation="fromTeam"
      :autoplay="{
        delay: delayVal,
        disableOnInteraction: true,
      }"
    >
      <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
        <div v-if="from === 'projects'">
          <card_fund :urll="slide.url" :idx="idx" :title="slide.title" />
        </div>
        <div v-if="from === 'team'">
          <card_member
            :urll="slide.url"
            :name="slide.name"
            :content="slide.content"
            :title="slide.title"
          />
        </div>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<script setup>
import { toRefs, onMounted, ref } from "vue";

const props = defineProps(["screenVal", "slides", "from"]);
const { screenVal, slides, from } = toRefs(props);
const fromTeam = ref(false);
const delayVal = ref(2000);

onMounted(() => {
  if (from.value === "team") {
    fromTeam.value = true;
    delayVal.value = 5000;
  }
});
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
