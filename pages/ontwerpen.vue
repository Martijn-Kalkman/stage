<template>
  <Header />
  <Intro :active-block="2" />
  <div class="container mx-auto bg-[#343434] text-white p-4 mt-12 rounded">
    <h2 class="font-bold text-3xl">Conceptualiseren</h2>
  </div>

  <div class="container mx-auto bg-[#343434] text-white p-4 mt-12 rounded">
    <h2 class="font-bold text-3xl">Ontwerpen en prototypen</h2>
  </div>
</template>

<script setup>
import Intro from "./components/intro.vue";
</script>
