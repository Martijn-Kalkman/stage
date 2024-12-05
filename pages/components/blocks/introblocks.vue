<template>
  <div
    class="flex items-center justify-center px-4 py-8 bg-[#FDFBD4] text-black font-bold text-4xl font-bold text-center rounded-2xl"
  >
    <div>
      <!-- Display the text -->
      <p>{{ text }}</p>

      <!-- Display the icon if provided -->
      <div v-if="icon" class="mt-2">
        <img :src="icon" alt="icon" class="w-16 mx-auto" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: false,
    },
  },
};
</script>
