<template>
  <Header />
  <Intro :active-block="2" />
  <div class="container mx-auto bg-red-600 mt-12 rounded">
    <h2 class="font-bold text-3xl">Technische kennis en analyse</h2>
  </div>
</template>

<script setup>
import Intro from "./components/intro.vue";
</script>
