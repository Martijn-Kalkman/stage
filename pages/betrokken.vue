<script setup lang="ts">
import Navbar from "./components/navbar.vue";
import OpenModal from "./components/openModal.vue";
</script>

<template>
  <Navbar />
  <OpenModal>
    <span class="text-xl text-white font-bold">- Lerend vermogen: </span>
    <p class="leading-relaxed pb-4 text-red-400 text-lg">
      Ik ben kritisch en streef ernaar het beste in mezelf en anderen naar boven
      te halen. Ik reflecteer structureel op eigen ervaringen en feedback vanuit
      het stagebedrijf en trek daaruit lessen voor de toekomst.
    </p>
    <span class="text-xl text-white font-bold"
      >- Maatschappelijke verantwoordelijkheid:
    </span>
    <p class="leading-relaxed pb-4 text-red-400 text-lg">
      Ik verdiep me naast de directe gebruikers ook in andere stakeholders en
      maatschappelijke ontwikkelingen. Ik kan maatschappelijke en ethische
      implicaties van producten waaraan ik meewerk benoemen, en er een
      onderbouwde mening over vormen.
    </p>
  </OpenModal>
  <div class="sm:ml-64 text-xl text-gray-300">
    <div class="mx-auto 2xl:w-6/12 p-4 mt-12">
      <div class="">
        <h1 class="text-6xl font-bold text-white text-center">Betrokken</h1>
      </div>
    </div>
  </div>
</template>
