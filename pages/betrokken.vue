<template>
  <Header />
  <Intro :active-block="4" />
  <div class="container mx-auto bg-[#343434] text-white p-4 mt-12 rounded">
    <h2 class="font-bold text-3xl">Lerend vermogen</h2>
  </div>

  <div class="container mx-auto bg-[#343434] text-white p-4 mt-12 rounded">
    <h2 class="font-bold text-3xl">Maatschappelijke verantwoordelijkheid</h2>
  </div>
</template>

<script setup>
import Intro from "./components/intro.vue";
</script>
