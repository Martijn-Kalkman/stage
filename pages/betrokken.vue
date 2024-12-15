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
        <span class="text-3xl text-white font-bold">- Lerend vermogen: </span>
        <h4 class="text-2xl mt-4 mb-4">- Terugblik</h4>
        <p>
          Tijdens het werken aan projecten probeer ik altijd het beste in mezelf
          naar boven te halen. Ik denk mee met klanten en werk goed samen met
          mijn partner. Ik vraag altijd om feedback tijdens, en wanneer ik klaar
          ben met een project, want het is altijd goed om te horen hoe iemand
          anders het zou aanpakken.
        </p>
        <h4 class="text-2xl mt-4 mb-4">- Vooruitzicht</h4>
        <span class="text-3xl text-white font-bold"
          >- Maatschappelijke verantwoordelijkheid
        </span>
        <h4 class="text-2xl mt-4 mb-4">- Terugblik</h4>
        <p class="mt-4">
          Tijdens mijn stage besteed ik veel aandacht aan drie belangrijke
          punten die een grote rol spelen bij het developen van websites en
          applicaties: security, privacy en accessibility. Deze onderwerpen zijn
          niet alleen belangrijk voor de klant, maar zo draag ik ook bij aan een
          veilige en toegankelijke ervaring voor gebruikers.
        </p>
        <p class="mt-4">
          Bij het ontwikkelen van websites zorg ik ervoor dat security altijd
          prioriteit krijgt. Een van de eerste stappen die ik neem, is het
          implementeren van HTTPS om ervoor te zorgen dat de gegevens die worden
          uitgewisseld tussen gebruikers en de website beveiligd zijn. Voordat
          er een website live gaat, test ik altijd via de owasp top 10 om te
          kijken of de website wel goed beveiligd is. Dit zorgt er voor dat de
          websites die ik maak veilig zijn.
        </p>
        <p class="mt-4">
          Privacy vind ik ook erg belangrijk. Het belangrijkste van privacy vind
          ik dat er goed wordt omgegaan met de gegevens van de eindgebruikers
          van de website. In mijn projecten verzamel ik alleen gegevens die
          noodzakelijk zijn, en ik gebruik altijd een duidelijke cookie-melding
          waarin gebruikers zelf kunnen aangeven welke gegevens ze willen delen.
          Dit zorgt voor vertrouwlijkheid, maar geeft gebruikers ook controle
          over hun eigen informatie.
        </p>
        <p class="mt-4">
          Accessibility is een ander onderdeel wat erg belangrijk is. Ik wil dat
          iedereen ongeacht beperkingen, toegang moet kunnen hebben tot de
          applicaties die ik bouw. Om dit te bereiken, volg ik de WCAG methode.
          Zo test ik mijn applicaties het kleurcontrast en voeg ik ALT tags toe
          aan afbeeldingen en zorg ik ervoor dat websites makkelijk te navigeren
          zijn met alleen een toetsenbord.
        </p>
        <h4 class="text-2xl mb-4">- Vooruitzicht</h4>
        <p class="mt-4">
          Deze focus op security, privacy en accessibility zorgt ervoor dat de
          websites en applicaties die ik maak niet alleen voldoen aan technische
          eisen, maar ook rekening houden met maatschappelijke en ethische
          verantwoordelijkheden. Dit helpt mij om professionele producten te
          leveren, en zo draag ik ook bij aan een veilige digitale wereld. In de
          toekomst wil ik meer testen gaan uitvoeren en er voor zorgen dat mijn
          websites voor elke groep bereikbaar is.
        </p>
      </div>
    </div>
  </div>
</template>
