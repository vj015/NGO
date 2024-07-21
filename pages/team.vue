<template>
  <div class="m-4 border-2 border-red-200">
    <Heading msg="Meet our team!" />
    <crousel
      screenVal="3"
      :slides="slides"
      from="team"
      class="hidden md:block"
    />
    <crousel screenVal="1" :slides="slides" from="projects" class="md:hidden" />
  </div>
</template>
<script setup>
const slides = [
  {
    url: "/team/Vipul Jain.png",
    title: "Founder & President",
    content: "",
  },
  {
    url: "/team/Vaishnavi Saxena.png",
    title: "Co-Founder & General Secretary",
    content: "",
  },
  {
    url: "/team/Sarthak Sharma.jpg",
    title: "Co-Founder & Vice President",
    content: "",
  },
  {
    url: "/team/Vaishnavi Dixit.jpg",
    title: "Member & Active Volunteer",
    content: "",
  },
  {
    url: "/team/Ridhima.jpg",
    title: "Member & Active Volunteer",
    content: "",
  },
  {
    url: "/team/Ragini Sahu.jpg",
    title: "Member & Active Volunteer",
    content: "",
  },
  {
    url: "/team/Khushi kaushik.png",
    title: "Member & Active Volunteer",
    content: "",
  },
  {
    url: "/team/Tanu Mishra.png",
    title: "Member & Active Volunteer",
    content: "",
  },
  {
    url: "/team/Priyanshi.png",
    title: "Member & Active Volunteer",
    content: "",
  },
];
</script>
