<template>
  <Intro :active-block="1" />
  <div class="container mx-auto bg-[#343434] text-white p-4 mt-12 rounded">
    <h2 class="font-bold text-3xl">Technische kennis en analyse</h2>
    <div class="flex lg:flex-row flex-col">
      <div class="lg:w-6/12 mb-4 lg:mb-0">
        <p class="mt-4">
          Voor de projecten van mijn bedrijf gebruik ik tegenwoordig vaak het
          framework NUXT. Dit doe ik omdat ik op deze manier een betere
          SEO-score kan halen op de websites die ik bouw. Het framework wordt
          nog steeds vaak geupdate, dus ik moet goed op de hoogte blijven van de
          nieuwste veranderingen.
        </p>
        <p class="mt-4">
          Omdat ik mijn code herbruikbaar en begrijpelijk wil maken, heb ik van
          mijn mentor het advies gekregen om geen commands meer te gebruiken in
          mijn code. Dit doe ik nu niet meer, omdat de code duidelijk moet zijn
          zonder commands. Als ik bijvoorbeeld een functie schrijf die
          gebruikers aan een database moet toevoegen, noem ik deze functie
          makkelijk addUsers. Deze functie moet dan ook alleen dat doen zodat
          iedereen het kan begrijpen.
        </p>
      </div>
      <div class="lg:w-6/12 px-4">
        <img class="h-96 rounded-lg" src="/ontwikel1.png" />
        <span>Code in NUXT</span>
      </div>
    </div>
  </div>

  <div class="container mx-auto bg-[#343434] text-white p-4 mt-12 rounded">
    <h2 class="font-bold text-3xl">Technische kennis en analyse</h2>
  </div>
</template>

<script setup>
import Intro from "./components/intro.vue";
</script>
