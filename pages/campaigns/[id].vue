<template>
  <div class="m-2">
    <Heading msg="Campaigns!" />
    <div class="flex flex-col">
      <div class="flex flex-col md:flex-row items-center justify-center m-5">
        <div
          class="md:w-1/2 text-center font-serif text-3xl mb-4 font-extrabold"
        >
          {{ slides[route.params.id].title }}
        </div>
        <div class="md:w-1/2 text-left">
          <p class="font-mono text-xl">
            {{ slides[route.params.id].content }}
          </p>
        </div>
      </div>
      <div class="flex flex-col items-center m-5">
        <iframe
          src="https://www.youtube.com/embed/bO0oHSqGfYA"
          title="आशा की किरण कहानी"
          class="w-full md:w-9/12 h-96"
        ></iframe>
      </div>
      <div class="flex flex-col md:flex-row items-center md:items-start m-5">
        <div class="md:w-1/2 text-left my-2 md:m-2">
          <Heading msg="Mission!" />
          <p class="font-mono text-xl">
            {{ slides[route.params.id].objective }}
          </p>
        </div>
        <div class="md:w-1/2 text-left my-2 md:m-2">
          <Heading msg="Vision!" />
          <p class="font-mono text-xl">
            {{ slides[route.params.id].conclusion }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const route = useRoute();
const slides = [
  {
    url: "/frame9.webp",
    title: "Each One, Adapt One",
    content:
      'The "Each One, Adopt One" campaign is an initiative aimed at fostering a sense of responsibility and community involvement by encouraging individuals to adopt and support the education of one underprivileged child. This campaign is grounded in the belief that everyone has the power to make a difference in someone elses life, and by providing educational opportunities, we can collectively uplift society.',
    objective:
      "At our nonprofit, we believe in the power of individual responsibility to create lasting change. We invite you to take personal responsibility for the education and welfare of one child, ensuring they receive quality education through our NGO. By adopting a child, you can help break the cycle of poverty and provide them with the necessary resources such as books and other educational materials. Our campaign goes beyond education by fostering a mentor-mentee relationship, allowing you to guide and support the child's overall development. Together, we can strengthen community ties and improve the welfare of children in our locality. Join us in making a difference today!",
    conclusion:
      'The "Each One, Adopt One" campaign by Asha Ki Kiran invites individuals or families to adopt a child by committing to a monthly donation of 200 Rs, supporting the childs education. Adopters receive regular updates and progress reports to ensure transparency and track the childs development. Additionally, a support system is in place to assist adopters with any challenges and provide necessary resources. This campaign aims to create a ripple effect, where each contribution significantly impacts a childs life, leading to a better-educated and empowered generation and ultimately contributing to the nations development.',
  },
  {
    url: "/fame6.webp",
    title: "Let's Leave No Child Uneducated",
    content:
      "In our ongoing commitment to ensuring that every child receives a quality education, we are thrilled to announce the Let's Leave No Child Uneducated campaign. This initiative focuses on distributing workbooks specifically designed for primary school children, addressing both their educational needs and personal development.",
    objective:
      "The objectives of the program include providing educational support by offering workbooks that cover fundamental subjects to ensure children have the necessary resources to excel academically, promoting personal development through activities and exercises that enhance critical thinking, creativity, and emotional intelligence for holistic growth, and ensuring accessibility by distributing these workbooks to underprivileged children in remote and underserved areas to bridge the gap in educational resources.",
    conclusion:
      "**Why Workbooks?** Workbooks are an effective tool for reinforcing classroom learning, offering structured exercises that children can work on independently or with minimal supervision, making them perfect for supplementing school education. Additionally, these workbooks are designed to be engaging and interactive, encouraging children to take an active interest in their studies. **How You Can Help:** We invite individuals, organizations, and businesses to join us in this noble cause. Your support can come in various forms: financial contributions to fund the production and distribution of workbooks, volunteering to help with the distribution and conduct follow-up sessions to ensure children are benefiting from the materials, and raising awareness about the campaign through social media, community events, and personal networks. Together, we can make a significant impact on the lives of many children, providing them with the tools they need to build a brighter future. Let's come together and leave no child uneducated.",
  },
  {
    url: "/fame5.webp",
    title: "Waste to Wonder: Transforming Trash into Treasures",
    content:
      "At Asha Ki Kiran, we believe in turning challenges into opportunities. Our latest initiative, Waste to Wonder, embodies this philosophy by focusing on transforming plastic waste into beautiful, useful goods. This innovative campaign aims to address environmental issues while empowering underprivileged children through the art of crafting.",
    objective:
      "The campaign aims to educate the community about the adverse effects of plastic waste and the importance of recycling and reusing materials, teach underprivileged children art and craft skills to create items from discarded plastic and waste materials, provide a platform for these children to showcase their creativity and skills, boosting their confidence and opening up potential future opportunities, and involve local communities in the collection and donation of plastic waste, fostering a sense of collective responsibility and participation.",
    conclusion:
      "This campaign features a range of activities, including regular workshops and training sessions where children learn to transform waste materials into decorative items, jewelry, and everyday products. It also organizes exhibitions to showcase these creations, with proceeds supporting further education and activities. Community clean-up events are held to collect plastic waste, accompanied by educational sessions on waste management and recycling. Additionally, the campaign partners with local artists and environmentalists to provide diverse perspectives and enrich the learning experience for the children. By merging creativity with sustainability, Waste to Wonder reduces plastic waste while fostering a sense of achievement and hope among young participants, significantly impacting both the environment and their lives.",
  },
];
</script>
