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
      <p
        class="text-xl mb-2 text-center font-semibold font-serif text-red-500 block capitalize"
      >
        {{ title }}
      </p>
      <button
        @click="btnClicked()"
        class="w-auto px-4 py-2 m-2 text-red-500 rounded font-mono text-xl border-2 border-red-500 hover:text-white hover:bg-red-500"
      >
        Explore
        <span class="inline-block align-middle"><IconsRightarrow /></span>
      </button>
    </div>
  </div>
</template>
<script setup>
import { toRefs } from "vue";

let props = defineProps(["urll", "title", "idx"]);
const { urll, title, idx } = toRefs(props);
async function btnClicked() {
  console.log("Button clicked");
  await navigateTo(`/campaigns/${idx.value}`);
}
</script>
