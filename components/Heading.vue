<template>
  <div class="m-2 text-xl md:text-2xl font-serif font-extrabold">
    {{ msg }}
  </div>
  <hr class="h-1 w-1/4 bg-red-200 m-2" />
</template>
<script setup>
const prop = defineProps({
  msg: String,
});
</script>
