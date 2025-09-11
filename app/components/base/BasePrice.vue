<template>
  <div
    class="anim-bg card-with-light relative p-6 flex flex-col items-center justify-center md:min-h-[270px] h-full rounded-2xl overflow-hidden w-full text-black"
  >
    <div class="flex justify-center mb-4">
      <img
        v-if="image"
        :src="image"
        :alt="title"
        class="w-[33px] h-[23px] lg:w-[60px] lg:h-[41px] md:w-auto flex-shrink-0"
      />
    </div>

    <div class="relative z-10 text-center flex flex-col items-center w-full">
      <div class="flex flex-col items-center w-full mb-4">
        <h3
          class="text-lg md:text-3xl font-geist font-bold text-white lg:whitespace-nowrap overflow-hidden text-ellipsis"
        >
          {{ title }}
        </h3>
        <hr class="border-t border-white/30 w-full mt-2 max-w-xs" />
      </div>

      <p
        class="text-white text-sm md:text-lg font-geist opacity-90 text-center max-w-md"
      >
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