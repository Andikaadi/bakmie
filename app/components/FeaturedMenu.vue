<script setup lang="ts">
const menus = [
  {
    nama: 'Bakmie Kampoeng',
    harga: 'Rp18.000',
    gambar: '/images/bakmie_jamurayam.png'
  },
  {
    nama: 'Bakmie Kobar',
    harga: 'Rp22.000',
    gambar: '/images/bakmie_kobar.png'
  },
  {
    nama: 'Bakmie Jamur ayam',
    harga: 'Rp25.000',
    gambar: '/images/bakmie_ayamkatsu.png'
  }
]
</script>

<template>
  <section class="py-24">
    <div class="max-w-7xl mx-auto px-6">

      <div class="text-center mb-14">

        <span class="text-green-700 font-semibold">
          Menu Andalan
        </span>

        <h2 class="text-5xl font-bold text-green-900 mt-4">
          Menu Favorit Pelanggan
        </h2>

        <p class="mt-4 text-gray-600">
          Cita rasa khas kampung dengan bahan pilihan terbaik.
        </p>

      </div>

      <div class="grid md:grid-cols-3 gap-8">

        <div
          v-for="menu in menus"
          :key="menu.nama"
          class="bg-white rounded-3xl overflow-hidden shadow-lg hover:-translate-y-2 transition"
        >
          <img
            :src="menu.gambar"
            :alt="menu.nama"
            class="w-full h-64 object-contain bg-[#f8f5ec]"
          >

          <div class="p-6 text-center">

            <h3 class="text-2xl font-bold text-green-900">
              {{ menu.nama }}
            </h3>

            <p class="mt-2 text-yellow-600 font-bold">
              {{ menu.harga }}
            </p>

          </div>

        </div>

      </div>

    </div>
  </section>
</template>