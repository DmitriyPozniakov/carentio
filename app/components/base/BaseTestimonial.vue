<template>
  <div
    class="relative z-10 testimonial-bg card-shadow p-4 py-8 md:p-8 lg:min-h-[430px]"
  >
    <div class="flex justify-center mb-6">
      <div class="w-20 h-20 xl:w-32 xl:h-32 rounded-full overflow-hidden">
        <img :src="avatar" :alt="name" class="w-full h-full object-cover" />
      </div>
    </div>

    <div class="flex justify-between items-start gap-6 mb-2 lg:mb-8">
      <button
        class="hover:opacity-70 transition-opacity"
        @click="$emit('prev')"
      >
        <img
          src="/images/arrow.svg"
          alt="Previous"
          class="w-12 h-12 rotate-180 brightness-0 invert"
        />
      </button>

      <h3
        class="text-white font-geist text-xl xl:text-2xl font-medium text-center border-b-2 border-[#3B7B63]"
      >
        {{ name }}
      </h3>
      <button
        class="hover:opacity-70 transition-opacity"
        @click="$emit('next')"
      >
        <img
          src="/images/arrow.svg"
          alt="Next"
          class="w-12 h-12 brightness-0 invert"
        />
      </button>
    </div>

    <div class="flex items-center justify-center">
      <p
        class="text-white font-geist text-lg md:text-2xl md:font-extralight leading-relaxed opacity-90 max-w-[1000px] text-left md:text-center"
      >
        {{ text }}
      </p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  avatar: String,
  text: String,
});
defineEmits(["prev", "next"]);
</script>
