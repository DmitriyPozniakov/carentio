<template>
  <section class="py-12">
    <h2 class="heading font-geist">
      Korzyści dla <span class="sub-heading">Ciebie</span>
    </h2>

    <div class="flex flex-col items-center xl:flex-row gap-8">
      <div
        class="flex flex-col gap-4 md:grid md:grid-cols-3 md:gap-4 xl:flex xl:flex-col w-full xl:max-w-[400px]  mx-auto"
      >
        <div
          v-for="(benefit, index) in benefits"
          :key="index"
          class="custom-card xl:max-h-[150px] bg-white text-center p-4 rounded-lg shadow w-full"
        >
          <h3 class="text-base font-roboto font-semibold mb-2 text-[#001F02]">
            {{ benefit.heading }}
          </h3>
          <p class="text-custom-green font-roboto">{{ benefit.article }}</p>
        </div>
      </div>

      <div
        class="bg-hero-radial flex-1 min-h-[1000px] text-white items-center justify-center rounded-4xl hidden xl:flex"
      >
        placeholder
      </div>
    </div>
  </section>
</template>


<script setup lang="ts">
const benefits = [
  {
    heading: "Rezerwacje bez komplikacji",
    article:
      "dodawaj i edytuj rezerwacje w kilka kliknięć, monitoruj dostępność floty i nigdy nie przegap okazji do wynajmu.",
  },
  {
    heading: "Szybkie wydania i zwroty",
    article:
      "automatyczne protokoły wydania i zwrotu w kilka chwil, zero błędów, zero stresu. Twoi klienci docenią płynny proces, a Ty oszczędzisz czas.",
  },
  {
    heading: "Flota pod pełną kontrolą",
    article:
      "rejestruj serwisy, wymiany opon, ubezpieczenia i wszystko, co potrzebne do sprawnego zarządzania pojazdami – bez zbędnych papierów.",
  },
  {
    heading: "Raporty, które mówią same za siebie",
    article:
      "sprawdź w czasie rzeczywistym, ile zarabia każdy pojazd i podejmuj decyzje, które maksymalizują Twój zysk.",
  },
  {
    heading: "Pełna kontrola nad klientami",
    article:
      "zarządzaj bazą klientów, przyznawaj rabaty i natychmiast identyfikuj „niesolidnych” najemców. Z Carentio zawsze wiesz, komu możesz zaufać.",
  },
];
</script>
