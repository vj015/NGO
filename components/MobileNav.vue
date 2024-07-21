<template>
  <div
    class="bg-white customh md:hidden w-full text-center font-extrabold border-red-500 font-mono text-4xl flex flex-col items-center justify-around flex-wrap"
  >
    <div class="flex flex-col">
      <button
        @click="handleredirect(1)"
        class="bg-transparent hover:bg-yellow-200 text-red-600 sha font-semibold hover:text-white py-2 px-4 border border-red-600 hover:border-red-600 rounded my-4"
      >
        Home
      </button>
      <button
        @click="handleredirect(2)"
        class="bg-transparent hover:bg-yellow-200 text-red-600 sha font-semibold hover:text-white py-2 px-4 border border-red-600 hover:border-red-600 rounded my-4"
      >
        About us
      </button>
      <button
        @click="handleredirect(3)"
        class="bg-transparent hover:bg-yellow-200 text-red-600 sha font-semibold hover:text-white py-2 px-4 border border-red-600 hover:border-red-600 rounded my-4"
      >
        Meet our Team
      </button>
      <button
        @click="handleredirect(4)"
        class="bg-transparent hover:bg-yellow-200 text-red-600 sha font-semibold hover:text-white py-2 px-4 border border-red-600 hover:border-red-600 rounded my-4"
      >
        Contact
      </button>
    </div>
    <sociallinks class="" />
  </div>
</template>
<script setup>
const emit = defineEmits();
async function handleredirect(idx) {
  switch (idx) {
    case 1:
      await navigateTo("/");
      break;
    case 2:
      await navigateTo("/about");
      break;
    case 3:
      await navigateTo("/team");
      break;
    case 4:
      await navigateTo("/contact");
      break;
    default:
      await navigateTo("/");
      break;
  }
  emit("signal-nav");
}
</script>
<style scoped>
.customh {
  height: 87vh;
}
.sha {
  text-shadow: 2px 2px #ff0000;
}
</style>
