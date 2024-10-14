<!-- Intro.vue -->
<template>
  <img
    class="absolute w-full h-[900px] opacity-30 object-cover z-[-1]"
    src="../../public/leaf.png"
  />
  <div class="h-[900px]">
    <div class="lg:container relative mx-auto">
      <nav class="flex justify-between items-center p-4">
        <!-- Logo / Brand -->
        <NuxtLink to="/" class="text-2xl font-bold">
          Stage Martijn Kalkman
        </NuxtLink>

        <!-- Hamburger Icon for Mobile Screens -->
        <div class="lg:hidden">
          <button
            id="menu-toggle"
            class="text-3xl focus:outline-none"
            @click="menuOpen = !menuOpen"
          >
            &#9776;
            <!-- Hamburger Icon -->
          </button>
        </div>

        <!-- Links - Hidden on Small Screens -->
        <div class="hidden lg:flex space-x-4 text-lg">
          <NuxtLink to="ontwikkelen" class="hover:underline">
            Ontwikkelen
          </NuxtLink>
          <NuxtLink to="ontwerpen" class="hover:underline">Ontwerpen</NuxtLink>
          <NuxtLink to="ondernemen" class="hover:underline"
            >Ondernemen</NuxtLink
          >
          <NuxtLink to="betrokken" class="hover:underline">Betrokken</NuxtLink>
        </div>

        <!-- Mobile Menu - Visible on Small Screens -->
        <div
          class="absolute top-16 left-0 right-0 bg-white lg:hidden"
          :class="{ hidden: !menuOpen }"
        >
          <div class="flex flex-col items-center space-y-4 p-4">
            <NuxtLink to="ontwikkelen" class="hover:underline">
              Ontwikkelen
            </NuxtLink>
            <NuxtLink to="ontwerpen" class="hover:underline"
              >Ontwerpen</NuxtLink
            >
            <NuxtLink to="ondernemen" class="hover:underline"
              >Ondernemen</NuxtLink
            >
            <NuxtLink to="betrokken" class="hover:underline"
              >Betrokken</NuxtLink
            >
          </div>
        </div>
      </nav>
    </div>
    <section class="z-50">
      <div
        class="bg-[#343434] mx-2 lg:mx-auto lg:container mx-auto h-[40rem] rounded-2xl w-12/12 flex items-center"
      >
        <div class="flex lg:flex-row flex-col text-white w-full">
          <div class="lg:w-6/12 my-auto mx-auto">
            <h1
              class="lg:w-[30rem] mx-auto font-bold text-4xl text-center lg:text-left lg:text-5xl"
            >
              Stage bij LeafyLines
            </h1>
            <p class="lg:w-[30rem] px-2 lg:px-0 mt-8 mx-auto">
              Bij LeafyLines maken we een professionele website die bij de klant
              past. We zorgen ervoor dat alles goed geregeld is, van het ontwerp
              tot de website. Bij Leafylines staan we klaar om te helpen bij
              elke stap van het proces, voor professionele en responsive
              websites.
            </p>
          </div>

          <div class="lg:w-6/12 px-2 lg:px-0 flex items-center justify-center">
            <img src="/leafylines1.png" class="max-w-full h-96" />
          </div>
        </div>
      </div>

      <div
        class="flex lg:flex-row flex-col lg:container mx-auto px-2 lg:px-20 flex-row"
      >
        <Block
          title="Ontwikkelen"
          icon="custom:gear"
          :active="activeBlock === 1"
          nuxtlink="ontwikkelen"
        />
        <Block
          title="Ontwerpen"
          icon="custom:ontwerpen"
          :active="activeBlock === 2"
          nuxtlink="ontwerpen"
        />
        <Block
          title="Ondernemen"
          icon="custom:ondernemen"
          :active="activeBlock === 3"
          nuxtlink="ondernemen"
        />
        <Block
          title="Betrokken"
          icon="custom:betrokken"
          :active="activeBlock === 4"
          nuxtlink="betrokken"
        />
      </div>
    </section>
  </div>
</template>

<script setup>
import Block from "./block.vue";
import { ref } from "vue";

const menuOpen = ref(false);

const props = defineProps({
  activeBlock: {
    type: Number,
    default: 0,
  },
});
</script>
