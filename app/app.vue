
<template>
  <div class="max-w-[1440px] mx-auto px-[20px] py-[24px] md:p-[24px]">
    <Navigation />
    <Hero />
    <Benefits />
    <Review />
  </div>
</template>

<script setup lang="ts">
import Hero from "./components/sections/Hero.vue";
import Benefits from "./components/sections/Benefits.vue";
import Review from "./components/sections/Review.vue";
</script>
