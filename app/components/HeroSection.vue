<template>
  <section class="bg-[#F8F5EC]">

    <div class="
    max-w-7xl mx-auto
    px-6 py-16
    grid
    md:grid-cols-2
    gap-10
    items-center
  ">

      <!-- Kiri -->
      <div>

        <span class="bg-green-100 text-green-800 px-4 py-2 rounded-full font-semibold">
          Sejak 1998
        </span>

        <h1 class="
    text-4xl
    md:text-6xl
    font-bold
    text-green-900
  ">
          Bakmie Kampoeng
        </h1>

        <p class="mt-6 text-lg text-gray-600 leading-relaxed">
        </p>

        <nuxt-link to="/menu" class="mt-8 bg-green-800 text-white px-6 py-3 rounded-xl hover:bg-green-900 transition">
          Lihat Menu
        </nuxt-link>

      </div>

      <!-- Kanan -->
      <div class="flex justify-center">

        <img src="/images/bakmie_kampoeng.png" class="
    w-full
    max-w-[350px]
    mx-auto
  ">

      </div>

    </div>

  </section>
</template>