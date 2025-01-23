<script setup lang="ts">
import Navbar from "./components/navbar.vue";
</script>

<template>
  <Navbar />
  <div class="sm:ml-64 text-xl text-gray-300">
    <div class="mx-auto 2xl:w-6/12 p-4 mt-12">
      <div class="">
        <h1 class="text-6xl font-bold text-white text-center">Projecten</h1>
        <div class="flex flex-row">
          <NuxtLink class="bg-red-900 w-6/12 m-4 rounded-xl" to="/hilo">
            <img class="h-72 object-cover rounded-xl" src="/hilo.png" />
          </NuxtLink>
          <div class="bg-red-900 w-6/12 m-4 rounded-xl"></div>
        </div>
      </div>
    </div>
  </div>
</template>
