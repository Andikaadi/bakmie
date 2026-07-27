<template>
  <div class="bg-[#F8F5EC] min-h-screen">

    <Navbar />

    <section class="max-w-5xl mx-auto px-6 py-20">

      <div class="text-center mb-16">

        <h1 class="text-5xl font-bold text-green-900">
          Hubungi Kami
        </h1>

        <p class="mt-4 text-gray-600">
          Kami siap melayani dan menerima pesanan Anda.
        </p>

      </div>

      <div class="grid md:grid-cols-2 gap-8">

        <!-- Informasi -->
        <div
          class="
            bg-white
            p-8
            rounded-3xl
            shadow-lg
          "
        >

          <h2 class="text-2xl font-bold text-green-900 mb-6">
            Informasi
          </h2>

          <div class="space-y-4">

            <p>
              📍 8GHW+CCQ, Made, Pacet, Kec. Pacet, Kabupaten Mojokerto, Jawa Timur 61374
            </p>

            <p>
              📞 0812-3456-7890
            </p>

            <p>
              🕒 Buka Selasa - Minggu
              <br>
              09.00 - 21.00 WIB
            </p>

          </div>

        </div>

        <!-- Sosial Media -->
        <div
          class="
            bg-white
            p-8
            rounded-3xl
            shadow-lg
          "
        >

          <h2 class="text-2xl font-bold text-green-900 mb-6">
            Sosial Media
          </h2>

          <div class="flex flex-col gap-4">

            <a
              href="https://www.instagram.com/bakmiekampoeng.pct?igsh=ZzJwczNmdnBsN3U0"
              target="_blank"
              class="
                bg-pink-500
                text-white
                p-4
                rounded-2xl
                font-semibold
                text-center
                hover:opacity-90
              "
            >
              📷 Instagram
            </a>

            <a
              href="https://www.tiktok.com/@bakmiekampoengpacet?_r=1&_t=ZS-98OAKcxiZKW"
              target="_blank"
              class="
                bg-black
                text-white
                p-4
                rounded-2xl
                font-semibold
                text-center
                hover:opacity-90
              "
            >
              🎵 TikTok
            </a>

            <a
              href="https://wa.me/6285645970955"
              target="_blank"
              class="
                bg-green-600
                text-white
                p-4
                rounded-2xl
                font-semibold
                text-center
                hover:opacity-90
              "
            >
              💬 WhatsApp
            </a>

          </div>

        </div>

      </div>

      <!-- Maps -->
      <div
        class="
          mt-10
          bg-white
          p-4
          rounded-3xl
          shadow-lg
        "
      >

        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3954.1092000781846!2d112.54354867602532!3d-7.671408192345344!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e78770003a77edf%3A0xf32a6fc4ef15fb04!2sBakmie%20Kampoeng%20Pacet!5e0!3m2!1sid!2sid!4v1785175225546!5m2!1sid!2sid"
          width="100%"
          height="400"
          style="border:0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          class="rounded-2xl"
        ></iframe>

      </div>

    </section>

    <Footer />

  </div>
</template>