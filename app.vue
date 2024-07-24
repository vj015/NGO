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
useHead({
  title: "Asha Ki Kiran Foundation - NGO",
  meta: [
    {
      name: "description",
      content:
        "🌍Educating 120 + kids currently,one step at a time. Till now provided food to 5000+ people. Together, Lets make a better world🧡",
    },
    {
      name: "keywords",
      content:
        "Asha Ki Kiran Foundation, Asha Ki Kiran, AshakikiranFoundation, ashakikiranfoundation, asha ki kiran foundation, children, ngo, NGO, Child NGO, Donation, Kanpur, help, needy",
    },
    { property: "og:title", content: "Asha Ki Kiran Foundation - NGO" },
    {
      property: "og:description",
      content:
        "🌍Educating 120 + kids currently,one step at a time. Till now provided food to 5000+ people. Together, Lets make a better world🧡",
    },
    {
      property: "og:image",
      content: "https://ashakikiranfoundation.org/BG/BG-3.webp",
    },
    { property: "og:url", content: "https://ashakikiranfoundation.org/" },
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "Asha Ki Kiran Foundation - NGO" },
    {
      name: "twitter:description",
      content:
        "🌍Educating 120 + kids currently,one step at a time. Till now provided food to 5000+ people. Together, Lets make a better world🧡",
    },
    {
      name: "twitter:image",
      content: "https://ashakikiranfoundation.org/BG/BG-3.webp",
    },
  ],
  script: [
    {
      hid: "gtag",
      src: "https://www.googletagmanager.com/gtag/js?id=G-6H5GYT4SP3",
      async: true,
    },
    {
      hid: "gtag-inline",
      innerHTML: `
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'G-6H5GYT4SP3');
      `,
    },
  ],
});

useSeoMeta({
  title: "Asha Ki Kiran Foundation - NGO",
  ogTitle: "Asha Ki Kiran Foundation - NGO",
  description:
    "🌍Educating 120 + kids currently,one step at a time. Till now provided food to 5000+ people. Together, Lets make a better world🧡",
  ogDescription:
    "🌍Educating 120 + kids currently,one step at a time. Till now provided food to 5000+ people. Together, Lets make a better world🧡",
  ogImage: "https://ashakikiranfoundation.org/BG/BG-3.webp",
  ogUrl: "https://ashakikiranfoundation.org/",
});
</script>
