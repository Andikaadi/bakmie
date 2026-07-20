<template>
  <nav class="bg-green-900 text-white shadow-lg">
    <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">

      <div class="flex items-center gap-3">

        <img src="/images/logo.png" alt="Logo Bakmie Kampoeng" class="w-12 h-12 object-contain">

        <div>
          <h1 class="text-3xl font-bold">
            Bakmie Kampoeng
          </h1>

          <p class="text-sm text-green-200">
            Sejak 1998
          </p>
        </div>

      </div>

      <ul class="hidden md:flex gap-8 font-medium">
        <NuxtLink to="/">Beranda</NuxtLink>
        <NuxtLink to="/menu">Menu</NuxtLink>
        <NuxtLink to="/tentang">Tentang</NuxtLink>
        <NuxtLink to="/galeri">Galeri</NuxtLink>
        <NuxtLink to="/kontak">Kontak</NuxtLink>
      </ul>

      <button class="bg-yellow-400 text-green-900 px-5 py-2 rounded-lg font-bold hover:scale-105 transition">
        Pesan Sekarang
      </button>

    </div>
  </nav>
</template>