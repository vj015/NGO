<template>
  <Navbar @mobile-nav-open="mobilenavopen" />
  <div v-show="!showNav">
    <NuxtPage />
  </div>
  <Donate
    v-show="!showNav && !(route.name === 'donate' || route.name === 'join-us')"
  />
  <Footer v-show="!showNav" />
</template>
<script setup lang="ts">
const route = useRoute();
const showNav = ref(false);
function mobilenavopen(val = false) {
  showNav.value = val;
}
useSeoMeta({
  title: "Asha Ki Kiran",
  ogTitle: "Asha Ki Kiran",
  description: "NGO which serves humanity and childcare",
  ogDescription: "NGO which serves humanity and childcare",
  ogImage: "/logo1.webp",
});
</script>
