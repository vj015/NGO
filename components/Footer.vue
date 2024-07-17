<template>
  <div
    class="max-h-full max-w-full bg-slate-900 text-slate-300 font-serif md:px-12 p-12 pb-0"
  >
    <div class="max-w-4xl mx-auto flex flex-col items-center justify-center">
      <h1 class="text-2xl sm:text-4xl leading-tight font-mono">
        {{ "Send us a Message!" }}
      </h1>
      <div class="max-w-full md:w-5/6">
        <MessageForm />
      </div>
    </div>
    <div
      class="flex flex-col justify-center items-center md:flex-row md:justify-between mx-auto gap-3"
    >
      <div class="flex flex-col justify-center items-start md:w-4/12 my-4">
        <p class="font-bold mb-2 text-xl">
          {{ "Copyright "
          }}<span class="inline-block align-middle"><copyright /></span
          >{{ " 2024 Asha ki Kiran Foundation" }}
        </p>
        <p class="font-mono text-xl">
          {{
            "Asha ki Kiran Foundation is an award-winning organization working hard to address the issue of Child Education of BPL in India. "
          }}<span class="inline-block text-stone-500">{{
            "Read more...."
          }}</span>
        </p>
      </div>
      <div class="flex flex-col items-center my-4">
        <h1 class="m-4 text-6xl formathead text-nowrap overflow-hidden">
          {{ "Asha ki Kiran" }}
        </h1>
        <p class="font-mono">
          {{ "Made with " }}<span class="text-red-600">❤</span>{{ " in India" }}
        </p>
        <div class="flex flex-row items-center flex-wrap">
          <button
            href="#"
            class="w-auto px-4 py-2 m-2 md:text-right text-red-500 rounded font-mono text-xs md:text-xl border-2 border-red-500 hover:text-white hover:bg-red-500"
          >
            Join us
          </button>
          <button
            href="#"
            class="w-auto px-4 py-2 m-2 md:text-right text-white bg-red-500 rounded font-mono text-xs md:text-xl border-2 border-red-500 hover:text-red-500 hover:bg-slate-900"
          >
            Donate
          </button>
        </div>
      </div>
      <div class="flex flex-col justify-center items-start md:w-4/12 my-4">
        <p class="font-bold mb-2 text-xl">
          {{ "Address" }}
        </p>
        <p class="font-mono text-xl">
          {{
            "201-202, Atlanta Centre, Sonawala Road, Goregaon East, Mumbai 400063, Maharashtra, India."
          }}
        </p>
        <sociallinks class="md:w-4/12 my-4" />
      </div>
    </div>
    <!-- <div class="flex justify-center items-center m-auto text-xs">
      {{ "Meet the developer for more!" }}
    </div> -->
  </div>
</template>
<script setup>
import MessageForm from "/components/MessageForm.vue";
import sociallinks from "/components/sociallinks.vue";
import copyright from "/components/icons/copyright.vue";
</script>
<style>
.formathead {
  font-family: "Sacramento", cursive;
  text-transform: none;
  font-weight: 400;
  color: #fe0002 !important;
  font-size: 3em !important;
}
</style>
