<script setup lang="ts">
import Navbar from "./components/navbar.vue";
</script>

<template>
  <Navbar />
  <div class="sm:ml-64 text-xl text-gray-300">
    <div class="mx-auto 2xl:w-6/12 p-4">
      <div class="">
        <h1 class="text-6xl font-bold text-center">
          Uitwisselingsbezoek bij DIGIWEDO
        </h1>
        <img
          class="mt-4 shadow-white border-b-[10px] border-r-[12px] rounded-xl border-gray-800 transition-all duration-300 hover:border-b-0 hover:border-r-0"
          src="/digiwedo.jpg"
          alt="Floating Image"
        />
        <p class="mt-4">
          Tijdens de stage-terugkomdag heb ik een bezoek gebracht aan DIGIWEDO,
          een bedrijf met een design- en developmentteam dat dagelijks werkt aan
          websites. Het is een middelgroot bedrijf met ongeveer 10-15
          medewerkers. Binnen DIGIWEDO wordt voornamelijk gebruikgemaakt van
          WordPress, een CMS-systeem dat het makkelijker maakt om websites te
          bouwen en klanten in staat stelt deze zelf te beheren. Voor meer
          vrijheid gebruiken ze binnen WordPress de Oxygen Builder, waarmee je
          alsnog zelf code kunt schrijven en meer mogelijkheden hebt binnen de
          websites.
        </p>
        <p class="mt-4">
          Als ik DIGIWEDO vergelijk met mijnbedrijf, merk ik dat ik minder ben
          van WordPress. Ik heb er al vaker mee heb gewerkt, maar ik vind de
          beperkte vrijheid om volledig custom websites te maken een groot
          nadeel. Wat ik wel neter vind van DIGIWEDO is dat er een duidelijke
          scheiding is tussen de design- en developmentafdelingen. Hierdoor
          kunnen developers zich beter focussen op de technische kant, terwijl
          designers zich kunnen focusen op het maken van betere ontwerpen.
        </p>
        <p class="mt-4">
          Ook krijgt DIGIWEDOenorm veel feedback. Soms ontvangen ze meer dan
          tien feedbackrondes per project, wat laat zien hoe goed ze luisteren
          naar de wensen van hun klanten.
        </p>
        <div class="flex lg:flex-row flex-col">
          <div class="lg:w-6/12 p-4">
            <img
              class="mt-4 shadow-white border-b-[10px] border-r-[12px] rounded-xl border-gray-800 transition-all duration-300 hover:border-b-0 hover:border-r-0"
              src="/DIGIWEDOselfie.jpg"
              alt="Floating Image"
            />
          </div>
          <div class="lg:w-6/12 p-4">
            <img
              class="mt-4 shadow-white border-b-[10px] border-r-[12px] rounded-xl border-gray-800 transition-all duration-300 hover:border-b-0 hover:border-r-0"
              src="/DIGIWEDOgroup.jpg"
              alt="Floating Image"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
