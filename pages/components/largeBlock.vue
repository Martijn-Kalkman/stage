<template>
  <div :class="alignEnd ? 'flex justify-end' : 'flex justify-start'">
    <div
      class="bg-[#343434] shadow-lg shadow-black shadow-b-2xl shadow-r-2xl my-10 h-[30rem] rounded-2xl w-9/12 flex items-center"
    ></div>
  </div>
</template>

<script setup>
const props = defineProps({
  alignEnd: {
    type: Boolean,
    default: true,
  },
});
</script>
