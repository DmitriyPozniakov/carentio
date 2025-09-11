<template>
  <section class="mb-16">
    <h2 class="heading mb-8 font-geist">
      Opinie <span class="sub-heading">Klientów</span>
    </h2>

    <Swiper
      :modules="[Pagination]"
      :slides-per-view="1"
      :space-between="30"
      loop
      class="w-full h-full"
      @swiper="onSwiper"
    >
      <SwiperSlide
        v-for="(review, i) in reviews"
        :key="i"
        class="w-full h-full flex items-center justify-center"
      >
        <BaseTestimonial
          :name="review.name"
          :avatar="review.avatar"
          :text="review.text"
          @prev="goPrev"
          @next="goNext"
        />
      </SwiperSlide>
    </Swiper>
  </section>
</template>
<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

import BaseTestimonial from "@/components/base/BaseTestimonial.vue";
import { ref } from "vue";

const swiperRef = ref(null);

const onSwiper = (swiper) => {
  swiperRef.value = swiper;
};

const goPrev = () => {
  swiperRef.value?.slidePrev();
};

const goNext = () => {
  swiperRef.value?.slideNext();
};

const reviews = [
  {
    name: "Mike, Dubai",
    avatar: "/images/man.svg",
    text: `Before Carentio, managing rentals was eating up hours of my week.
Now I save time and cut costs effortlessly — every vehicle's
performance and every client's details are just a click away.`,
  },
  {
    name: "Mike, Dubai",
    avatar: "/images/man.svg",
    text: `Before Carentio, managing rentals was eating up hours of my week.
Now I save time and cut costs effortlessly — every vehicle's
performance and every client's details are just a click away.`,
  },
  {
    name: "Mike, Dubai",
    avatar: "/images/man.svg",
    text: `Before Carentio, managing rentals was eating up hours of my week.
Now I save time and cut costs effortlessly — every vehicle's
performance and every client's details are just a click away.`,
  },
];
</script>
