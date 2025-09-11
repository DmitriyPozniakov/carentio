<template>
  <div
    class="anim-bg  relative p-6 flex flex-row md:flex-col gap-3 items-center md:min-h-[270px] justify-between md:justify-center rounded-2xl overflow-hidden w-full h-full"
  >
    <img
      v-if="image"
      :src="image"
      :alt="title"
      class="w-[33px] h-[23px] lg:w-[60px] lg:h-[41px] justify-self-start md:w-auto flex-shrink-0"
    />

    <div class="relative z-10 text-center md:text-center">
      <h3 class="text-xl md:text-3xl font-geist font-bold text-white">
        {{ title }}
      </h3>
      <p class="text-white text-sm md:text-lg font-geist opacity-90">
        {{ text }}
      </p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  image: String,
  title: String,
  text: String
})
</script>

