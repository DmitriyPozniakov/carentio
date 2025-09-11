<template>
  <section class="py-4 lg:py-12">
    <div
      class="flex flex-col md:grid md:grid-cols-3 grid-rows-[auto_1fr_1fr] gap-6 w-full h-full"
    >
      <h2
        class="heading font-geist mb-0 font-light md:col-span-2 md:row-start-1 lg:text-[68px] text-center md:text-center pb-2 lg:border-b border-[#ccddda]"
      >
        Cennik stworzony<span class="hidden lg:inline"><br /></span> z myślą
        <span class="sub-heading">o Tobie</span>
      </h2>
      <div
        class="md:col-span-2 md:row-start-2 md:row-span-2 flex flex-col justify-center lg:justify-end h-full gap-6"
      >
        <div
          class="grid grid-cols-1 sm:grid-cols-2 gap-4 md:p-6 rounded-2xl"
        >
          <div v-for="(card, index) in cards" :key="index">
            <BasePrice
              :image="card.image"
              :title="card.title"
              :text="card.text"
            />
          </div>
        </div>
      </div>
      <div
        class="md:col-span-1 md:row-start-1 md:row-span-3 flex flex-col justify-between h-auto md:h-full"
      >
        <div class="relative w-full flex justify-center">
          <img
            src="/images/phone.png"
            alt="Phone Mockup"
            class="hidden lg:block w-full max-w-[420px] h-auto relative z-20 pointer-events-none"
          />
          <div
            class="hidden lg:flex absolute inset-0 lg:px-4 lg:py-3 xl:px-8 py-4 items-center justify-center z-10"
          >
            <Form />
          </div>
          <div class="lg:hidden w-full"><Form /></div>
        </div>
      </div>
    </div>
  </section>
</template> 

<script setup>
import BasePrice from "../base/BasePrice.vue";
const cards = [
  {
    image: "/images/Car.svg",
    title: "Tylko 10 zł / samochód",
    text: "prosta, przejrzysta i uczciwa cena.",
  },
  {
    image: "/images/Block.svg",
    title: "Bez żadnej ceny minimalnej",
    text: " płacisz tylko za to, czego naprawdę używasz.",
  },
  {
    image: "/images/People.svg",
    title: "Floty powyżej 100 aut?",
    text: "przygotujemy indywidualną ofertę dopasowaną do Twoich potrzeb i maksymalnego zysku.",
  },
  {
    image: "/images/Stonks.svg",
    title: "Konkurencja? Droższa",
    text: "my stawiamy na uczciwość i prostotę.",
  },
];
</script>