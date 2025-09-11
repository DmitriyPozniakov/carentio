<template>
  <div
    class="anim-bg card-with-light relative p-6 flex flex-row md:flex-col items-center md:min-h-[270px] rounded-2xl overflow-hidden w-full h-full text-black"
  >
    <div class="flex-1 flex justify-start md:justify-center">
      <img
        v-if="image"
        :src="image"
        :alt="title"
        class="w-[33px] h-[23px] lg:w-[60px] lg:h-[41px] md:w-auto flex-shrink-0"
      />
    </div>

    <div class="flex-[2] relative z-10 text-left md:text-center">
      <h3
        class="text-lg md:text-3xl font-geist font-bold text-white whitespace-nowrap overflow-hidden text-ellipsis"
      >
        {{ title }}
      </h3>
      <p class="text-white text-sm md:text-lg font-geist opacity-90">
        {{ text }}
      </p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: String,
  image: String,
  text: String,
});
</script>
