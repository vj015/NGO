<template>
  <div class="m-4 border-2 border-red-200">
    <Heading msg="Meet our team!" />
    <crousel
      screenVal="3"
      :slides="slides"
      from="team"
      class="hidden md:block"
    />
    <crousel screenVal="1" :slides="slides" from="team" class="md:hidden" />
  </div>
</template>
<script setup>
const slides = [
  {
    url: "/team/Vipul Jain.png",
    name: "Vipul Jain",
    title: "Founder & President",
    content:
      "Vipul Jain is the visionary founder of Asha Ki Kiran, committed to transforming society through education and various humanitarian campaigns. He currently operates three free education centers across different locations, providing free education to 200 children, and is deeply dedicated to making a positive impact in the community.",
  },
  {
    url: "/team/Vaishnavi Saxena.png",
    name: "Vaishnavi Saxena",
    title: "Co-Founder & General Secretary",
    content:
      "Vaishnavi Saxena is the co-founder and general secretary of Asha Ki Kiran handling all backend operations. She is the mastermind behind many campaigns and efficiently manages all our online platforms, ensuring smooth and effective communication and coordination.",
  },
  {
    url: "/team/Sarthak Sharma.jpg",
    name: "Sarthak Sharma",
    title: "Co-Founder & Vice President",
    content:
      "Sarthak Sharma is the co-founder and vice president of our NGO. He oversees all operations and is responsible for fundraising to support various social work campaigns, ensuring the successful execution and sustainability of our initiatives.",
  },
  {
    url: "/team/Vaishnavi Dixit.jpg",
    name: "Vaishnavi Dixit",
    title: "Member & Active Volunteer",
    content:
      "Vaishnavi Dixit is an active social worker who has been with Asha Ki Kiran for the past 2 years. She has participated in numerous activities and campaigns and now leads a project of Asha Ki Kiran Waste2Wonder that focuses on creating art and craft from waste and plastic, promoting sustainability and creativity.",
  },
  {
    url: "/team/Ridhima.jpg",
    name: "Ridhima Gupta",
    title: "Member & Active Volunteer",
    content:
      "Ridhima Gupta is an active social worker engaged in various social causes across India. She is a valued member of the Asha Ki Kiran family. In collaboration with her NGO, Asha Ki Kiran operates one of its centers located in Panki, working together to make a positive impact in the community.",
  },
  {
    url: "/team/Ragini Sahu.jpg",
    name: "Ragini Sahu",
    title: "Member & Active Volunteer",
    content:
      "Ragini Sahu, a dedicated graduate currently preparing for government services, An active volunteer at Asha Ki Kiran. She contributes to social causes and shares her knowledge as a teacher at Akk Kakadev Classes, exemplifying her commitment to education and community service.",
  },
  {
    url: "/team/Khushi kaushik.png",
    name: "Khushi Kaushik",
    title: "Member & Active Volunteer",
    content:
      "Khushi Kaushik is a dedicated 3rd-year student at Armapur PG College. Alongside her studies, she actively volunteers at Asha Ki Kiran, contributing to various social causes. Additionally, she imparts knowledge and teaches at Akk Kakadev Classes, demonstrating her commitment to education and community service.",
  },
  {
    url: "/team/Tanu Mishra.png",
    name: "Tanu Mishra",
    title: "Member & Active Volunteer",
    content:
      "Tanu Mishra is a dedicated student pursuing her post-graduation. Alongside her academic endeavors, she actively volunteers at Asha Ki Kiran, contributing to various social causes. She also shares her knowledge and passion for teaching at Akk Kakadev Classes, demonstrating her commitment to education and community service.",
  },
  {
    url: "/team/Priyanshi.png",
    name: "Priyanshi",
    title: "Member & Active Volunteer",
    content:
      "Priyanshi is a dedicated 12th-grade student. In addition to her studies, she actively volunteers at Asha Ki Kiran, contributing to social causes. She also imparts knowledge as a teacher at Akk Kakadev Classes, showcasing her commitment to education and community service.",
  },
];
</script>
