<template>
  <div>
    <nav class="flex flex-wrap items-center justify-between md:px-5">
      <img src="/logo.jpg" class="w-28" />
      <div
        class="hidden w-full md:w-auto md:flex text-right mt-5 md:mt-0 border-red-500 font-mono text-2xl"
      >
        <a
          href="#"
          class="block md:inline-block text-red-900 px-3 py-3 hover:border-b-4 border-red-500"
          >Home</a
        >
        <a
          href="#"
          class="block md:inline-block text-red-900 px-3 py-3 hover:border-b-4 border-red-500"
          >About</a
        >
        <a
          href="#"
          class="block md:inline-block text-red-900 px-3 py-3 hover:border-b-4 border-red-500"
          >Fundraising</a
        >
        <a
          href="#"
          class="block md:inline-block text-red-900 px-3 py-3 hover:border-b-4 border-red-500"
          >Contact</a
        >
      </div>
      <div class="flex flex-row items-center flex-wrap">
        <button
          href="#"
          class="w-auto px-4 py-2 m-2 md:text-right text-red-500 rounded font-mono text-xs md:text-xl border-2 border-red-500 hover:text-white hover:bg-red-500"
        >
          Join us
        </button>
        <button
          href="#"
          class="w-auto px-4 py-2 m-2 md:text-right text-white bg-red-500 rounded font-mono text-xs md:text-xl border-2 border-red-500 hover:text-red-500 hover:bg-white"
        >
          Donate
        </button>
        <sidebar
          @click="toggleNav()"
          class="w-auto m-2 md:hidden"
          v-if="!showNav"
        />
        <cross
          @click="toggleNav()"
          class="w-auto m-2 md:hidden"
          v-if="showNav"
        />
      </div>
    </nav>
    <div
      class="bg-white h-screen md:hidden w-full text-center font-extrabold mt-5 border-red-500 font-mono text-4xl"
      v-if="showNav"
    >
      <a href="#" class="block text-red-900 px-3 py-6">Home</a>
      <a href="#" class="block text-red-900 px-3 py-6">About</a>
      <a href="#" class="block text-red-900 px-3 py-6">Fundraising</a>
      <a href="#" class="block text-red-900 px-3 py-6">Contact</a>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import sidebar from "/components/icons/sidebar.vue";
import cross from "/components/icons/cross.vue";
const showNav = ref(false);
function toggleNav() {
  showNav.value = !showNav.value;
}
</script>
