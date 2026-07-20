<script setup lang="ts">
defineProps<{
    menu: {
        id: number
        nama: string
        harga: string
        gambar: string
    }
}>()
</script>

<template>
    <div class="bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300">

        <img :src="menu.gambar" :alt="menu.nama" class="w-full h-60 object-cover" />

        <div class="p-5">

            <h3 class="text-2xl font-bold text-green-900">
                {{ menu.nama }}
            </h3>

            <p class="text-yellow-600 font-bold mt-2">
                {{ menu.harga }}
            </p>

            <button class="mt-4 bg-green-800 text-white px-4 py-2 rounded-lg hover:bg-green-900">
                Pesan Sekarang
            </button>

        </div>

    </div>
</template>