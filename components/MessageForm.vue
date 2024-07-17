<template>
  <div class="card h-fit max-w-6xl p-5 mb-2" id="form" v-if="showForm">
    <form @submit.prevent="submit">
      <div class="mb-6">
        <div class="mx-0 mb-1 sm:mb-4">
          <div class="mx-0 mb-1 sm:mb-4">
            <label
              for="name"
              class="pb-1 text-xs uppercase tracking-wider"
            ></label
            ><input
              type="text"
              id="name"
              autocomplete="given-name"
              placeholder="Your name"
              class="mb-2 w-full rounded-md border border-slate-300 text-slate-900 py-2 pl-2 pr-4 shadow-md sm:mb-0"
              name="name"
              required="true"
              minlength="2"
            />
          </div>
        </div>
        <div class="mx-0 mb-1 sm:mb-4">
          <label
            for="textarea"
            class="pb-1 text-xs uppercase tracking-wider"
          ></label
          ><textarea
            id="textarea"
            name="textarea"
            cols="30"
            rows="5"
            placeholder="Write your message..."
            required="true"
            minlength="5"
            class="mb-2 w-full rounded-md border border-slate-300 py-2 pl-2 pr-4 shadow-md text-slate-900 sm:mb-0"
          ></textarea>
        </div>
      </div>
      <div class="text-center">
        <button
          type="submit"
          class="w-full bg-slate-300 text-slate-900 px-6 py-3 font-xl rounded-md sm:mb-0 font-mono"
        >
          Send Message
        </button>
      </div>
    </form>
  </div>
  <div class="flex justify-center my-24" v-if="!showForm">
    <h1 class="m-4 text-6xl formathead">
      {{ "Thank you! We'll revert you shortly." }}
    </h1>
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
  color: #c1cad7 !important;
  font-size: 3em !important;
}
</style>
