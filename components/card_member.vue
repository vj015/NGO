<template>
  <div
    class="w-72 bg-white shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl"
  >
    <img
      :src="urll"
      alt="Campaign"
      class="h-80 w-72 object-cover rounded-t-xl"
    />
    <div class="px-4 py-3 w-72 flex flex-col items-center">
      <p class="text-3xl underline text-center formathead23 block capitalize">
        {{ name }}
      </p>
      <p
        class="text-xs mb-2 text-center font-bold font-serif text-red-500 block capitalize"
      >
        {{ title }}
      </p>
      <p
        class="text-xs mb-2 text-center font-serif text-red-300 block"
      >
        {{ content }}
      </p>
    </div>
  </div>
</template>
<script setup>
import { toRefs } from "vue";

let props = defineProps(["urll", "title", "name", "content"]);
const { urll, title, name, content } = toRefs(props);
</script>
<style scoped>
.formathead23 {
  font-family: "Sacramento", cursive;
  text-transform: none;
  font-weight: 400;
  color: #fe0002 !important;
}
</style>
