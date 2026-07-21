<script setup lang="ts">
import { ref } from 'vue'

const isOpen = ref(false)

const menus = [
  { nama: 'Beranda', link: '/' },
  { nama: 'Menu', link: '/menu' },
  { nama: 'Tentang', link: '/tentang' },
  { nama: 'Galeri', link: '/galeri' },
  { nama: 'Kontak', link: '/kontak' }
]
</script>

<template>
  <header
    class="
      sticky
      top-0
      z-50
      bg-[#F8F5EC]/90
      backdrop-blur-md
      border-b
      border-green-100
    "
  >
    <div
      class="
        max-w-7xl
        mx-auto
        px-5
        h-20
        flex
        items-center
        justify-between
      "
    >

      <!-- Logo -->

      <NuxtLink
        to="/"
        class="flex items-center gap-3"
      >

        <img
          src="/images/logo.png"
          class="w-12 h-12 object-contain"
        >

        <div>

          <h1
            class="
              text-xl
              font-bold
              text-green-900
            "
          >
            Bakmie Kampoeng
          </h1>

          <p
            class="
              text-xs
              text-gray-500
            "
          >
            Authentic Noodle
          </p>

        </div>

      </NuxtLink>

      <!-- Desktop -->

      <nav
        class="
          hidden
          md:flex
          gap-8
          font-semibold
        "
      >

        <NuxtLink
          v-for="menu in menus"
          :key="menu.nama"
          :to="menu.link"
          class="
            text-green-900
            hover:text-yellow-600
            transition
          "
        >
          {{ menu.nama }}
        </NuxtLink>

      </nav>

      <!-- Tombol -->

      <NuxtLink
        to="/menu"
        class="
          hidden
          md:block
          bg-green-800
          hover:bg-green-900
          text-white
          px-6
          py-3
          rounded-full
          font-semibold
          transition
        "
      >
        Pesan Sekarang
      </NuxtLink>

      <!-- Mobile -->

      <button
        @click="isOpen=!isOpen"
        class="
          md:hidden
          text-green-900
        "
      >

        <svg
          v-if="!isOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="w-8 h-8"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>

        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="w-8 h-8"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>

      </button>

    </div>

    <!-- Mobile Menu -->

    <transition
      enter-active-class="duration-300"
      leave-active-class="duration-200"
      enter-from-class="opacity-0 -translate-y-5"
      enter-to-class="opacity-100 translate-y-0"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-5"
    >

      <div
        v-if="isOpen"
        class="
          md:hidden
          bg-white
          border-t
        "
      >

        <NuxtLink
          v-for="menu in menus"
          :key="menu.nama"
          :to="menu.link"
          @click="isOpen=false"
          class="
            block
            px-6
            py-4
            border-b
            hover:bg-green-50
            text-green-900
          "
        >
          {{ menu.nama }}
        </NuxtLink>

      </div>

    </transition>

  </header>
</template>