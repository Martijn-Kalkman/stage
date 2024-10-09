<template>
  <NuxtLink
    :to="nuxtlink"
    :class="[
      'w-3/12 text-white text-center p-4 mx-8 -mt-20 rounded-2xl h-52',
      active ? 'bg-gray-500' : 'bg-[#72A97B]',
    ]"
  >
    <h4 class="text-4xl font-bold">{{ title }}</h4>
    <div class="flex mt-8 justify-center h-full">
      <Icon class="w-20 h-20" :name="icon" />
    </div>
  </NuxtLink>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  icon: {
    type: String,
    required: true,
  },
  active: {
    type: Boolean,
    default: false,
  },
  nuxtlink: {
    type: String,
    required: false,
  },
});
</script>
