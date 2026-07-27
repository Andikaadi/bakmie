<script setup lang="ts">
import { galeri } from '~/data/galeri'
</script>

<template>
  <div class="bg-[#F8F5EC] min-h-screen">

    <Navbar />

    <!-- Header -->
    <section class="py-20 text-center">

      <h1
        class="
          text-4xl
          md:text-6xl
          font-bold
          text-green-900
        "
      >
        Galeri Bakmie Kampoeng
      </h1>

      <p
        class="
          mt-4
          text-gray-600
          max-w-2xl
          mx-auto
        "
      >
        Lihat berbagai suasana nyaman
        di Bakmie Kampoeng.
      </p>

    </section>

    <!-- Galeri -->
    <section
      class="
        max-w-7xl
        mx-auto
        px-6
        pb-20
      "
    >

      <div
        class="
          grid
          grid-cols-2
          md:grid-cols-3
          gap-5
        "
      >

        <div
          v-for="item in galeri"
          :key="item.judul"
          class="
            group
            overflow-hidden
            rounded-3xl
            shadow-lg
            bg-white
          "
        >

          <div class="overflow-hidden">

            <img
              :src="item.gambar"
              :alt="item.judul"
              class="
                w-full
                aspect-square
                object-cover
                group-hover:scale-110
                transition
                duration-500
              "
            >

          </div>

          <div class="p-4">

            <h3
              class="
                text-center
                font-semibold
                text-green-900
              "
            >
              {{ item.judul }}
            </h3>

          </div>

        </div>

      </div>

    </section>

    <Footer />

  </div>
</template>