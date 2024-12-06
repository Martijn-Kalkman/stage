<script setup lang="ts">
import Navbar from "./components/navbar.vue";
import OpenModal from "./components/openModal.vue";
</script>

<template>
  <Navbar />
  <OpenModal>
    <span class="text-xl text-white font-bold">- Conceptualiseren: </span>
    <p class="leading-relaxed pb-4 text-red-400 text-lg">
      Ik ben in staat me te verdiepen in de probleemstelling en de doelgroep. Ik
      pas creatieve technieken toe om tot verschillende ideeën te komen en een
      concept te ontwerpen dat relevant is voor deze doelgroep.
    </p>
    <span class="text-xl text-white font-bold"
      >- Ontwerpen en prototypen:
    </span>
    <p class="leading-relaxed pb-4 text-red-400 text-lg">
      Ik kan vanuit userstories een interactieontwerp opstellen als basis voor
      verschillende prototypes. Middels gestructureerde gebruikerstesten doe ik
      aanbevelingen om tot een product te komen dat aanluit bij de doelgroep.
    </p>
  </OpenModal>
  <div class="sm:ml-64 text-xl text-gray-300">
    <div class="mx-auto 2xl:w-6/12 p-4 mt-12">
      <div class="">
        <h1 class="text-6xl font-bold text-white text-center">Ontwerpen</h1>
      </div>
    </div>
  </div>
</template>
