<template>
  <div class="m-2">
    <Heading msg="Join us!" />
    <div class="mx-auto my-8 md:w-1/2 border border-red-300 bg-white" v-if="showForm">
      <div class="p-5 space-y-5 shadow-xl">
        <form @submit.prevent="submit">
          <div class="grid grid-cols-2 gap-5">
            <input
              type="text"
              class="border border-red-300 px-4 py-2 focus:outline-none focus:border-red-500"
              placeholder="First Name"
            />
            <input
              type="text"
              class="border border-red-300 px-4 py-2 focus:outline-none focus:border-red-500"
              placeholder="Last Name"
            />
            <input
              type="email"
              class="border border-red-300 px-4 py-2 focus:outline-none focus:border-red-500 col-span-2"
              placeholder="Email"
            />
            <input
              type="tel"
              class="border border-red-300 px-4 py-2 focus:outline-none focus:border-red-500 col-span-2"
              placeholder="Phone"
            />
            <textarea
              cols="10"
              rows="5"
              class="border border-red-300 px-4 py-2 focus:outline-none focus:border-red-500 col-span-2"
              placeholder="Why you want to join us?"
            ></textarea>
          </div>
          <input
            type="submit"
            value="Request to Join"
            class="focus:outline-none mt-5 bg-red-500 px-4 py-2 text-white font-bold w-full"
          />
        </form>
      </div>
    </div>
    <div class="flex justify-center my-24" v-if="!showForm">
      <h1 class="m-4 text-2xl md:text-6xl formathead text-center">
        {{ "Thank you! We'll revert you shortly." }}
      </h1>
    </div>
  </div>
</template>
<script setup>
const showForm = ref(true);
const submit = async (e) => {
  e.preventDefault();
  showForm.value = false;
  await useFetch(
    `https://docs.google.com/forms/u/0/d/e/1FAIpQLSdJ_JetHkMNYSpPyiWf2pcw0W4C7P5QUYWYGSVBvXc_UAs1aA/formResponse?&submit=Submit?usp=pp_url&entry.175308092=${e.target[0].value}&entry.332484750=${e.target[1].value}&entry.2094425495=${e.target[2].value}`,
    {
      method: "POST",
    }
  );
};
</script>
<style scoped>
.formathead {
  font-family: "Sacramento", cursive;
  text-transform: none;
  font-weight: 400;
  color: #fe0002 !important;
}
</style>
