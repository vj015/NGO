<template>
  <div class="w-full mx-auto p-2 relative">
    <img src="/CTA.png" class="w-full" />
    <div
      class="absolute top-0 left-0 w-full h-full flex flex-col items-center justify-center text-xl md:text-5xl"
    >
      <div class="formathead">
        {{ "Make a Difference: Donate & Volunteer Today!" }}
      </div>
      <div class="flex flex-row items-center flex-wrap">
        <button
          href="#"
          class="w-auto px-4 py-2 m-2 md:text-right text-white rounded font-mono text-xs md:text-xl border-2 border-white"
        >
          Join us
        </button>
        <button
          href="#"
          class="w-auto px-4 py-2 m-2 md:text-right text-amber-900 bg-white rounded font-mono text-xs md:text-xl border-2 border-inherit"
        >
          Donate
        </button>
      </div>
    </div>
  </div>
</template>
<style>
.formathead {
  font-family: "Sacramento", cursive;
  text-transform: none;
  font-weight: 400;
  color: #ffffff !important;
  text-decoration: underline;
}
</style>
