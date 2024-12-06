<script setup lang="ts">
import Navbar from "./components/navbar.vue";
import OpenModal from "./components/openModal.vue";
</script>

<template>
  <Navbar />
  <OpenModal>
    <span class="text-xl text-white font-bold"
      >- Ondernemende houding en vaardigheden:
    </span>
    <p class="leading-relaxed pb-4 text-red-400 text-lg">
      Ik kijk verder dan wat me gevraagd wordt. Ik bedenk nieuwe oplossingen, en
      vergelijk met bestaande oplossingen en kom uit mezelf met adviezen om
      waarde te creëren voor de klant of het stagebedrijf.
    </p>
    <span class="text-xl text-white font-bold"
      >- Projectmatig werken en communiceren:
    </span>
    <p class="leading-relaxed pb-4 text-red-400 text-lg">
      Ik ben in staat om zowel individueel als in teamverband te werken om zo
      deadlines en afspraken na te komen. Ik kan hierin diverse rollen aannemen,
      vraag tijdig hulp en communiceer duidelijk met belanghebbenden.
    </p>
  </OpenModal>
  <div class="sm:ml-64 text-xl text-gray-300">
    <div class="mx-auto 2xl:w-6/12 p-4 mt-12">
      <div class="">
        <h1 class="text-6xl font-bold text-white text-center">Ondernemen</h1>
      </div>
    </div>
  </div>
</template>
