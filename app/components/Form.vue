<template>
  <form
    class="form-bg py-[51px] z-1 px-5 rounded-3xl h-full w-full flex flex-col justify-center"
  >
    <h2 class="text-white text-4xl font-geist font-black uppercase text-center pb-3 border-b border-[#1a6561] mb-6">
      Skontakuj się
    </h2>
    <p class="text-lg font-geist text-justify font-thin text-white border-b border-[#1a6561] pb-3 w-full mb-8">
      Wypełnij formularz i skontaktujemy się z Tobą, z ofertą.
      <span class="font-normal">Rozmowa potrwa tylko 5 minut.</span>
    </p>
    <div class="flex flex-col items-center gap-5">
      <input class="base-input font-geist placeholder-white font-light" placeholder="Nazwa wypożyczalni:" type="text" />
      <input class="base-input font-geist placeholder-white font-light" placeholder="Imię:" type="text" />
      <input class="base-input font-geist placeholder-white font-light" placeholder="Numer telefonu:" type="text" />
      <input class="base-input font-geist placeholder-white font-light" placeholder="Adres email:" type="text" />
      <button
        class="base-input font-geist flex items-center justify-center cursor-pointer transition transform hover:-translate-y-1"
      >
        Wyślij wiadomość
      </button>
    </div>
  </form>
</template>
