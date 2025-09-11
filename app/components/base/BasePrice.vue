<template>
  <div
    class="relative p-6 flex flex-row md:flex-col gap-3 items-center md:min-h-[270px] justify-between md:justify-center rounded-2xl card-with-light card-bg overflow-hidden w-full h-full"
  >
    <!-- Картинка -->
    <img
      v-if="image"
      :src="image"
      :alt="title"
      class="w-[50px] lg:w-[70px] justify-self-start h-auto md:w-auto flex-shrink-0"
    />

    <!-- Текст -->
    <div class="relative z-10 text-center md:text-center">
      <h3 class="text-xl font-bold text-black">
        {{ title }}
      </h3>
      <p class="text-black opacity-90">
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
