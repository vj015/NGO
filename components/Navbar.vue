<template>
  <div>
    <nav
      class="flex flex-wrap items-center justify-between md:px-5 bg-transparent w-full"
    >
      <img src="/logo1.webp" class="w-28" />
      <div
        class="hidden w-full md:w-auto md:flex text-right mt-5 md:mt-0 border-red-500 font-mono text-2xl"
      >
        <a
          href="/"
          class="inline-block custom-red px-3 py-3 hover:border-b-4 border-red-500"
          >Home</a
        >
        <a
          href="/about"
          class="inline-block custom-red px-3 py-3 hover:border-b-4 border-red-500"
          >About</a
        >
        <a
          href="/team"
          class="inline-block custom-red px-3 py-3 hover:border-b-4 border-red-500"
          >Team</a
        >
        <a
          href="/contact"
          class="inline-block custom-red px-3 py-3 hover:border-b-4 border-red-500"
          >Contact</a
        >
      </div>
      <div class="flex flex-row items-center flex-wrap">
        <button
          v-show="route.name != 'join-us'"
          @click="helper('/join-us')"
          class="w-auto px-4 py-2 m-2 md:text-right text-red-500 rounded font-mono text-xs md:text-xl border-2 border-red-500 hover:text-white hover:bg-red-500"
        >
          Join us
        </button>
        <button
          v-show="route.name != 'donate'"
          @click="helper('/donate')"
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
    <MobileNav @signal-nav="toggleNav()" v-if="showNav" />
  </div>
</template>
<script setup>
import { ref } from "vue";
import sidebar from "/components/icons/sidebar.vue";
import cross from "/components/icons/cross.vue";
const showNav = ref(false);
const route = useRoute();
const emit = defineEmits();
function toggleNav() {
  showNav.value = !showNav.value;
}
async function helper(path) {
  if (showNav.value === true) {
    showNav.value = false;
  }
  await navigateTo(path);
}
watch(
  showNav,
  (value) => {
    emit("mobile-nav-open", value);
  },
  { deep: true, immediate: true }
);
</script>
