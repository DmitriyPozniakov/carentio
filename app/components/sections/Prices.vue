<template>
  <section class="py-12">
    <div
      class="grid grid-cols-1 md:grid-cols-3 grid-rows-[auto_1fr_1fr] gap-6 w-full h-full"
    >
      <!-- Заголовок над карточками (первые 2 колонки) -->
      <h2
        class="heading md:col-span-2 md:row-start-1 lg:text-[68px] text-center md:text-center mb-4"
      >
        Cennik stworzony<span class="hidden lg:inline"><br /></span> z myślą
        <span class="sub-heading">o Tobie</span>
      </h2>

      <!-- Карточки займут первые 2 колонки, 2-я и 3-я строки -->
      <div
        class="md:col-span-2 md:row-start-2 md:row-span-2 flex flex-col justify-between h-full gap-6"
      >
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
          <div v-for="(card, index) in cards" :key="index">
            <BasePrice
              :image="card.image"
              :title="card.title"
              :text="card.text"
            />
          </div>
        </div>
      </div>

      <!-- Форма в 3-й колонке, растягивается на все 3 строки -->
      <div
        class="md:col-span-1 md:row-start-1 md:row-span-3 flex flex-col justify-between h-full"
      >
        <Form />
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
