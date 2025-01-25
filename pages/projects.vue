<script setup lang="ts">
import Navbar from "./components/navbar.vue";
</script>

<template>
  <Navbar />
  <div class="sm:ml-64 text-xl text-gray-300">
    <div class="mx-auto 2xl:w-6/12 p-4 mt-12">
      <div class="">
        <h1 class="text-6xl font-bold text-white text-center">Projecten</h1>
        <div class="flex lg:flex-row flex-col">
          <NuxtLink class="lg:w-6/12 m-4 rounded-xl" to="/hilo">
            <img class="h-80 object-cover rounded-xl" src="/hilo.png" />
            HI-LO
          </NuxtLink>

          <NuxtLink class="lg:w-6/12 m-4 rounded-xl" to="/leafylines">
            <img
              class="h-80 mx-auto object-cover rounded-xl"
              src="/leafylinesSite.png"
            />
            LeafyLines
          </NuxtLink>
        </div>
        <div class="flex lg:flex-row flex-col">
          <NuxtLink class="lg:w-6/12 m-4 rounded-xl" to="/oosterwijkonderhoud">
            <img
              class="h-80 object-cover rounded-xl"
              src="/oosterwijkonderhoud.png"
            />
            Oosterwijk Onderhoud
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>
