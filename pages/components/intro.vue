<!-- Intro.vue -->
<template>
  <img
    class="absolute w-full h-[900px] opacity-30 object-cover z-[-1]"
    src="../../public/leaf.png"
  />
  <div class="h-[900px]">
    <div class="container relative mx-auto">
      <nav class="flex justify-between items-center p-4">
        <NuxtLink to="/" class="text-2xl font-bold"
          >Stage Martijn Kalkman</NuxtLink
        >
        <div class="flex space-x-4 text-lg">
          <NuxtLink to="ontwikkelen" class="hover:underline"
            >Ontwikkelen</NuxtLink
          >
          <NuxtLink to="ontwerpen" class="hover:underline">Ontwerpen</NuxtLink>
          <NuxtLink to="ondernemen" class="hover:underline"
            >Ondernemen</NuxtLink
          >
          <NuxtLink to="betrokken" class="hover:underline">Betrokken</NuxtLink>
        </div>
      </nav>
    </div>
    <section class="z-50">
      <div
        class="bg-[#343434] container mx-auto h-[40rem] rounded-2xl w-12/12 flex items-center"
      >
        <div class="flex flex-row text-white w-full">
          <div class="w-6/12 my-auto mx-auto">
            <h1 class="w-[30rem] mx-auto font-bold text-5xl">
              Stage bij LeafyLines
            </h1>
            <p class="w-[30rem] mt-8 mx-auto">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus
              nobis alias natus, corporis non numquam tempora dolore repellat,
              aut asperiores eveniet sunt consequuntur amet commodi enim
              delectus laborum voluptas iste.
            </p>
          </div>

          <div class="w-6/12 flex items-center justify-center">
            <img src="/leafylines1.png" class="max-w-full h-96" />
          </div>
        </div>
      </div>

      <div class="flex container mx-auto px-20 flex-row">
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

const props = defineProps({
  activeBlock: {
    type: Number,
    default: 0,
  },
});
</script>
