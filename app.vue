<template>
  <NavBar @mobile-nav-open="mobilenavopen" />
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
import NavBar from "../NGO/components/Navbar.vue";
import Footer from "../NGO/components/Footer.vue";
const showNav = ref(false);
function mobilenavopen(val = false) {
  showNav.value = val;
}
useSeoMeta({
  title: "Asha Ki Kiran",
  ogTitle: "Asha Ki Kiran",
  description: "NGO which serves humanity and childcare",
  ogDescription: "NGO which serves humanity and childcare",
  ogImage: "/logo.jpg",
});
</script>
