<template>
  <Header />
  <Intro />
  <div class="container mx-auto">
    <section class="flex flex-col">
      <largeBlock :alignEnd="false" />
      <largeBlock :alignEnd="true" />
      <largeBlock :alignEnd="false" />
      <largeBlock :alignEnd="true" />
    </section>
  </div>
</template>

<script setup>
import largeBlock from "./components/largeBlock.vue";
import Intro from "./components/intro.vue";
</script>
