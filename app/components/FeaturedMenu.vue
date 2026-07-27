<script setup lang="ts">
const menus = [
  {
    nama: 'Bakmie Jamur Ayam',
    harga: 'Rp15.000',
    gambar: '/images/bakmie_jamurayam.png'
  },
  {
    nama: 'Bakmie Kobar',
    harga: 'Rp12.000',
    gambar: '/images/bakmie_kobar.png'
  },
  {
    nama: 'Bakmie Ayam Katsu',
    harga: 'Rp17.000',
    gambar: '/images/bakmie_ayamkatsu.png'
  }
]
</script>

<template>
  <section class="py-14 md:py-24 bg-[#F8F5EC]">

    <div class="max-w-7xl mx-auto px-5 md:px-6">

      <!-- Heading -->

      <div class="text-center mb-10 md:mb-14">

        <span
          class="
            inline-block
            bg-green-100
            text-green-800
            px-4
            py-2
            rounded-full
            text-sm
            font-semibold
          "
        >
          Menu Andalan
        </span>

        <h2
          class="
            mt-5
            text-3xl
            sm:text-4xl
            md:text-5xl
            font-bold
            text-green-900
          "
        >
          Menu Favorit Pelanggan
        </h2>

        <p
          class="
            mt-4
            text-gray-600
            max-w-xl
            mx-auto
          "
        >
          Cita rasa khas kampoeng dengan bahan pilihan terbaik.
        </p>

      </div>

      <!-- Slider -->

      <div
        class="
          flex
          gap-5
          overflow-x-auto
          pb-3

          snap-x
          snap-mandatory
        "
      >

        <div
          v-for="menu in menus"
          :key="menu.nama"
          class="
            min-w-[240px]
            sm:min-w-[280px]
            md:min-w-[320px]

            bg-white

            rounded-3xl

            overflow-hidden

            shadow-lg

            hover:-translate-y-2
            hover:shadow-xl

            transition-all
            duration-300

            snap-start

            flex-shrink-0
          "
        >

          <!-- Foto -->

          <div class="bg-[#F8F5EC] p-5">

            <img
              :src="menu.gambar"
              :alt="menu.nama"
              class="
                w-full

                aspect-square

                object-contain
              "
            >

          </div>

          <!-- Isi -->

          <div class="p-5 text-center">

            <h3
              class="
                text-lg
                md:text-2xl

                font-bold

                text-green-900
              "
            >
              {{ menu.nama }}
            </h3>

            <p
              class="
                mt-3

                inline-block

                bg-yellow-400

                px-4
                py-2

                rounded-full

                font-bold

                text-green-900
              "
            >
              {{ menu.harga }}
            </p>

          </div>

        </div>

      </div>

      <!-- Petunjuk Mobile -->

      <div
        class="
          md:hidden

          text-center

          mt-5

          text-sm

          text-gray-500
        "
      >
        ← Geser untuk melihat menu lainnya →
      </div>

      <!-- Tombol -->

      <div class="text-center mt-10">

        <NuxtLink
          to="/menu"
          class="
            inline-flex
            items-center
            gap-2

            bg-green-800
            hover:bg-green-900

            text-white

            px-8
            py-4

            rounded-2xl

            font-semibold

            transition
          "
        >
          🍜 Lihat Semua Menu
        </NuxtLink>

      </div>

    </div>

  </section>
</template>