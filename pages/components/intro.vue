<script setup lang="ts">
import Introblocks from "./blocks/introblocks.vue";
import Navbar from "./navbar.vue";
import Square from "./blocks/introblocks.vue";
</script>

<template>
  <Navbar />
  <section class="relative h-screen text-white">
    <!-- Central Content -->
    <div
      class="2xl:absolute inset-0 flex items-center justify-center z-10 px-4"
    >
      <div class="mt-32 2xl:mt-0">
        <span class="text-3xl sm:text-2xl md:text-3xl lg:text-4xl"
          >Stage bij</span
        >
        <h1 class="2xl:text-9xl text-6xl md:text-8xl font-bold">LeafyLines</h1>
        <button
          class="mt-4 px-4 py-2 bg-black text-white rounded text-sm sm:text-base lg:text-lg"
        >
          Begin met lezen
        </button>
      </div>
    </div>

    <!-- Squares Around -->
    <div class="relative h-full px-8 2xl:w-full">
      <!-- Top-Left Square -->
      <div
        class="2xl:absolute top-20 p-4 2xl:p-0 sm:top-16 left-20 sm:left-10 lg:left-32"
      >
        <Square text="Ontwikkelen" icon="/betrokken.png" />
      </div>

      <!-- Top-Right Square -->
      <div
        class="2xl:absolute top-40 p-4 2xl:p-0 sm:top-32 right-20 sm:right-10 lg:right-32"
      >
        <Square text="Ondernemen" icon="/betrokken.png" />
      </div>

      <!-- Bottom-Left Square -->
      <div
        class="2xl:absolute bottom-20 p-4 2xl:p-0 sm:bottom-16 left-40 sm:left-20 lg:left-52"
      >
        <Square text="Ontwerpen" icon="/betrokken.png" />
      </div>

      <!-- Bottom-Right Square -->
      <div
        class="2xl:absolute bottom-20 p-4 2xl:p-0 sm:bottom-16 right-40 sm:right-20 lg:right-40"
      >
        <Square text="Betrokken" icon="/betrokken.png" />
      </div>
    </div>
  </section>
</template>
