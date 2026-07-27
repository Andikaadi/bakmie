<template>
  <section class="bg-[#F8F5EC]">

    <div
      class="
        max-w-7xl
        mx-auto

        px-5
        py-10

        md:px-6
        md:py-20

        grid
        md:grid-cols-2

        gap-8
        md:gap-12

        items-center
      "
    >

      <!-- FOTO -->
      <div
        class="
          order-1
          md:order-2

          flex
          justify-center
        "
      >

        <img
          src="/images/bakmie_kampoeng.png"
          alt="Bakmie Kampoeng"
          class="
            w-56
            sm:w-64
            md:w-full

            max-w-[260px]
            md:max-w-[450px]

            object-contain

            drop-shadow-2xl
          "
        >

      </div>

      <!-- TEKS -->
      <div
        class="
          order-2
          md:order-1

          text-center
          md:text-left
        "
      >

        <span
          class="
            inline-block

            bg-green-100
            text-green-800

            px-4
            py-2

            rounded-full

            font-semibold
            text-sm
          "
        >
          🍜 Resep turun-temurun
        </span>

        <h1
          class="
            mt-5

            text-3xl
            sm:text-4xl
            md:text-6xl

            font-bold

            text-green-900

            leading-tight
          "
        >
          Bakmie Kampoeng
        </h1>

        <p
          class="
            mt-5

            text-gray-600

            text-base
            md:text-lg

            leading-relaxed

            max-w-md

            mx-auto
            md:mx-0
          "
        >
          Nikmati bakmie dengan cita rasa khas kampoeng,
          dibuat dari bahan pilihan dan disajikan hangat
          untuk menemani setiap momen bersama keluarga.
        </p>

        <div
          class="
            mt-8

            flex
            flex-col
            sm:flex-row

            gap-3

            justify-center
            md:justify-start
          "
        >

          <NuxtLink
            to="/menu"
            class="
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
            🍜 Lihat Menu
          </NuxtLink>

          <NuxtLink
            to="/kontak"
            class="
              border-2
              border-green-800

              text-green-800

              px-8
              py-4

              rounded-2xl

              font-semibold

              hover:bg-green-800
              hover:text-white

              transition
            "
          >
            📍 Lokasi Kami
          </NuxtLink>

        </div>

      </div>

    </div>

  </section>
</template>