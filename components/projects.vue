<template>
  <div class="m-4 border-2 border-red-200">
    <Heading msg="Join Our Ongoing Campaigns for Change!" />
    <crousel
      screenVal="3"
      :slides="slides"
      from="projects"
      class="hidden md:block"
    />
    <crousel screenVal="1" :slides="slides" from="projects" class="md:hidden" />
  </div>
</template>
<script setup>
const slides = [
  {
    url: "/frame9.webp",
    title: "Each One, Adopt One",
    content: "",
  },
  {
    url: "/fame6.webp",
    title: "Let's Leave No Child Uneducated",
    content: "",
  },
  {
    url: "/fame5.webp",
    title: "Waste to Wonder: Transforming Trash into Treasures",
    content: "",
  },
];
</script>
