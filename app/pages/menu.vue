<script setup lang="ts">
import { menus } from '~/data/menu'

const kategori = [
  'Bakmie',
  'Nasi',
  'Minuman',
  'Camilan',
  'Extra Topping'
]
</script>

<template>
  <div class="bg-[#F8F5EC] min-h-screen">

    <Navbar />

    <!-- HEADER -->
    <section class="py-16 md:py-20 text-center">

      <h1
        class="
          text-4xl
          md:text-6xl
          font-bold
          text-green-900
        "
      >
        Daftar Menu
      </h1>

      <p
        class="
          mt-4
          text-gray-600
          text-sm
          md:text-lg
        "
      >
        Nikmati berbagai pilihan menu favorit Bakmie Kampoeng
      </p>

    </section>

    <!-- KATEGORI -->
    <section
      v-for="kat in kategori"
      :key="kat"
      class="max-w-7xl mx-auto px-4 md:px-6 mb-16"
    >

      <!-- Judul -->
      <div
        class="
          flex
          justify-between
          items-center
          mb-6
        "
      >

        <h2
          class="
            text-2xl
            md:text-4xl
            font-bold
            text-green-900
            border-l-8
            border-yellow-500
            pl-4
          "
        >
          {{ kat }}
        </h2>

        <span
          class="
            text-green-700
            text-sm
            font-semibold
          "
        >
          Geser →
        </span>

      </div>

      <!-- SLIDER -->
      <div
        class="
          flex
          gap-5
          overflow-x-auto
          pb-4
          snap-x
          snap-mandatory
        "
      >

        <div
          v-for="menu in menus.filter(item => item.kategori === kat)"
          :key="menu.nama"
          class="
            min-w-[280px]
            max-w-[280px]
            bg-white
            rounded-3xl
            shadow-lg
            overflow-hidden
            flex-shrink-0
            snap-start
            hover:-translate-y-2
            hover:shadow-2xl
            transition-all
            duration-300
          "
        >

          <!-- FOTO -->
          <div class="p-4">

            <img
              :src="menu.gambar"
              :alt="menu.nama"
              class="
                w-full
                aspect-square
                object-cover
                rounded-2xl
              "
            >

          </div>

          <!-- ISI -->
          <div class="px-5 pb-5">

            <h3
              class="
                text-xl
                font-bold
                text-green-900
              "
            >
              {{ menu.nama }}
            </h3>

            <p
              class="
                mt-2
                text-gray-600
                text-sm
                min-h-[60px]
              "
            >
              {{ menu.deskripsi }}
            </p>

            <div class="mt-4">

              <span
                class="
                  bg-yellow-400
                  text-green-900
                  px-4
                  py-2
                  rounded-full
                  font-bold
                  text-sm
                "
              >
                {{ menu.harga }}
              </span>

            </div>

          </div>

        </div>

      </div>

    </section>

    <Footer />

  </div>
</template>