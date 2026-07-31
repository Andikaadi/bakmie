<script setup lang="ts">
import { ref } from 'vue'

const isOpen = ref(false)

const menus = [
  { nama: 'Beranda', link: '/' },
  { nama: 'Menu', link: '/menu' },
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
      bg-[#F8F5EC]/95
      backdrop-blur-lg
      border-b
      border-green-100
      shadow-sm
    "
  >

    <div
      class="
        max-w-7xl
        mx-auto

        px-4
        md:px-6

        h-16
        md:h-20

        flex
        items-center
        justify-between
      "
    >

      <!-- Logo -->

      <NuxtLink
        to="/"
        class="flex items-center gap-2 md:gap-3"
      >

        <img
          src="/images/logo.png"
          alt="Bakmie Kampoeng"
          class="
            w-9
            h-9

            md:w-12
            md:h-12

            object-contain
          "
        >

        <div>

          <h1
            class="
              text-base
              md:text-xl

              font-bold
              text-green-900

              leading-none
            "
          >
            Bakmie Kampoeng Pacet
          </h1>

          <p
            class="
              hidden
              md:block

              text-xs
              text-gray-500
            "
          >
            Authentic Noodle
          </p>

        </div>

      </NuxtLink>

      <!-- Desktop Menu -->

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

      <!-- Desktop Button -->

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
        Lihat Menu
      </NuxtLink>

      <!-- Mobile Button -->

      <button
        @click="isOpen = !isOpen"
        class="
          md:hidden

          p-2

          rounded-xl

          text-green-900

          hover:bg-green-100
        "
      >

        <svg
          v-if="!isOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="w-7 h-7"
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
          class="w-7 h-7"
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
      enter-active-class="duration-300 ease-out"
      leave-active-class="duration-200 ease-in"
      enter-from-class="opacity-0 -translate-y-3"
      enter-to-class="opacity-100 translate-y-0"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-3"
    >

      <div
        v-if="isOpen"
        class="
          md:hidden

          bg-white

          border-t

          shadow-lg
        "
      >

        <div class="p-4 space-y-2">

          <NuxtLink
            v-for="menu in menus"
            :key="menu.nama"
            :to="menu.link"
            @click="isOpen = false"
            class="
              block

              px-4
              py-3

              rounded-xl

              text-green-900
              font-medium

              hover:bg-green-50
            "
          >
            {{ menu.nama }}
          </NuxtLink>

          <NuxtLink
            to="/menu"
            @click="isOpen = false"
            class="
              mt-3

              block

              text-center

              bg-green-800
              text-white

              py-3

              rounded-xl

              font-semibold
            "
          >
            🍜 Lihat Menu
          </NuxtLink>

        </div>

      </div>

    </transition>

  </header>
</template>