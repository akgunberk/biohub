<template>
  <div class="bg-white">
    <div class="relative">
      <div class="max-w-7xl mx-auto h-auto">
        <div
          class="relative z-10 pb-8 bg-white sm:pb-16 md:pb-20 lg:max-w-2xl lg:w-full lg:pb-28 xl:pb-32 lg:h-screen"
        >
          <svg
            class="hidden lg:block absolute right-0 inset-y-0 h-full w-48 text-white transform translate-x-1/2"
            fill="currentColor"
            viewBox="0 0 100 100"
            preserveAspectRatio="none"
            aria-hidden="true"
          >
            <polygon points="50,0 100,0 50,100 0,100" />
          </svg>

          <div class="relative pt-6 px-4 sm:px-6 lg:px-8">
            <nav
              class="relative flex items-center justify-between sm:h-10 lg:justify-start"
              aria-label="Global"
            >
              <div
                class="flex items-center flex-grow flex-shrink-0 lg:flex-grow-0"
              >
                <div class="flex items-center justify-between w-full md:w-auto">
                  <div class="-mr-2 flex items-center md:hidden">
                    <button
                      type="button"
                      class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                      aria-expanded="false"
                      @click="toggle()"
                    >
                      <span class="sr-only">Open main menu</span>
                      <svg
                        class="h-6 w-6"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M4 6h16M4 12h16M4 18h16"
                        />
                      </svg>
                    </button>
                  </div>
                </div>
              </div>
              <div class="hidden md:block md:ml-10 md:pr-4 md:space-x-8">
                <NuxtLink
                  to="/blog"
                  class="font-medium text-gray-500 hover:text-gray-900"
                  >Ürünler</NuxtLink
                >

                <NuxtLink
                  to="/blog"
                  class="font-medium text-gray-500 hover:text-gray-900"
                  >Ücretlendirme</NuxtLink
                >

                <NuxtLink
                  to="/blog"
                  class="font-medium text-gray-500 hover:text-gray-900"
                  >Mentorlarımız</NuxtLink
                >

                <NuxtLink
                  to="/blog"
                  class="font-medium text-gray-500 hover:text-gray-900"
                  >Biz Kimiz?</NuxtLink
                >

                <NuxtLink
                  to="/blog"
                  class="font-medium text-indigo-600 hover:text-accent"
                  >Üye Ol</NuxtLink
                >
              </div>
            </nav>
          </div>

          <div
            :class="
              mobileMenu ? 'max-h-full' : 'max-h-0 transform -translate-y-full'
            "
            class="absolute top-0 inset-x-0 p-2 origin-top-right md:hidden transition duration-300"
          >
            <div
              class="rounded-lg shadow-md bg-white ring-1 ring-black ring-opacity-5 overflow-hidden"
            >
              <div class="px-5 pt-4 flex items-center justify-between">
                <button
                  type="button"
                  class="bg-white ml-auto rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500"
                  @click="toggle()"
                >
                  <span class="sr-only">Close main menu</span>
                  <svg
                    class="h-6 w-6"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    aria-hidden="true"
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
              <div class="px-2 pt-2 pb-3 space-y-1">
                <NuxtLink
                  to="/"
                  class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
                  >Ürünler</NuxtLink
                >

                <NuxtLink
                  to="/"
                  class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
                  >Ücretlendirme</NuxtLink
                >

                <NuxtLink
                  to="/"
                  class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
                  >Mentorlarımız</NuxtLink
                >

                <NuxtLink
                  to="/"
                  class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
                  >Biz Kimiz?</NuxtLink
                >
                <NuxtLink
                  to="/blog"
                  class="block px-3 py-2 text-base font-medium text-accent bg-gray-50 hover:bg-gray-100"
                >
                  Üye Ol
                </NuxtLink>
              </div>
            </div>
          </div>

          <main
            class="mx-auto max-w-7xl p-4 sm:mt-12 sm:px-6 md:mt-20 lg:mt-30 lg:px-8 xl:mt-40"
          >
            <div class="sm:text-center lg:text-left">
              <h1
                class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl md:text-5xl"
              >
                <span class="block"
                  >Bio
                  <span class="text-indigo-500">Hub</span>
                </span>
                <span class="block xl:inline"> Share Your Lab </span>
              </h1>
              <p
                class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0"
              >
                BioHub tüm dünyada hizla gelisen bio girişimcilerinin bir araya
                gelip kaynaklarini ve güclerini birlestirdigi bir platformdur.
                Bu platformda diğer insanlarin kaynaklarini kiralayabilir,
                onlarla iletisime gecebilirsin!
              </p>
              <div
                class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start"
              >
                <div class="rounded-md shadow">
                  <a
                    href="#"
                    class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 md:py-4 md:text-lg md:px-10"
                  >
                    Daha Fazlasi
                  </a>
                </div>
                <div class="mt-3 sm:mt-0 sm:ml-3">
                  <a
                    href="#"
                    class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-indigo-700 bg-indigo-100 hover:bg-indigo-200 md:py-4 md:text-lg md:px-10"
                  >
                    Live demo
                  </a>
                </div>
              </div>
            </div>
          </main>
        </div>
      </div>
      <div class="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
        <img
          class="h-56 w-screen object-cover sm:h-72 md:h-96 lg:w-full lg:h-screen"
          src="~/assets/bg.jpg"
          alt=""
        />
      </div>
    </div>

    <div
      class="py-12 bg-white mt-12 flex items-center justify-center mx-auto container"
    >
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="lg:text-center">
          <h2
            class="text-base text-indigo-600 font-semibold tracking-wide uppercase"
          >
            Nasil Calisir?
          </h2>

          <p
            class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl"
          >
            BioHub seni ve ihtiyaclarini bilir
          </p>
          <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
            Hemen üye ol, bilgilerini ve calistigin alani paylas. Kullandigin ve
            ihtiyacin olan laboratuvar malzelemelerini ekle. Ondan sonrasi bizde
            merak etme!
          </p>
        </div>

        <div class="mt-10">
          <dl
            class="space-y-10 md:space-y-0 md:grid md:grid-cols-2 sm:gap-x-12 md:gap-y-20 items-center"
          >
            <div class="flex md:w-5/6">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
                >
                  <svg
                    class="h-6 w-6"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"
                    />
                  </svg>
                </div>
              </div>
              <div class="ml-4">
                <dt class="text-lg leading-6 font-medium text-gray-900">
                  Büyüyen sirketinin ihtiyaclarini karsilamakta zorlaniyor
                  musun?
                </dt>
                <dd class="mt-2 text-base text-gray-500">
                  Uzulme! BioHub'da ihtiyacin olan makinelere sahip endüstrinin
                  devleriyle tanisip onlardan kaynak kiralayabilirsin
                </dd>
              </div>
            </div>

            <div class="max-h-48">
              <div v-html="growthLogo" class="bg-rose-500"></div>
            </div>

            <div class="flex md:w-5/6">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
                >
                  <!-- Heroicon name: outline/scale -->
                  <svg
                    class="h-6 w-6"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3"
                    />
                  </svg>
                </div>
              </div>
              <div class="ml-4">
                <dt class="text-lg leading-6 font-medium text-gray-900">
                  Bir türlü fikrini gelistirecegin bir laboratuvar bulamiyor
                  musun?
                </dt>
                <dd class="mt-2 text-base text-gray-500">
                  Burada kendi labini kiralamak isteyen bir sürü sirket var.
                  Sadece onlara hangi calisma saatlerinin uygun oldugunu sorman
                  yeterli!
                </dd>
              </div>
            </div>

            <div v-html="bioLogo" class="w-auto"></div>

            <div class="flex md:w-5/6">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
                >
                  <!-- Heroicon name: outline/lightning-bolt -->
                  <svg
                    class="h-6 w-6"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M13 10V3L4 14h7v7l9-11h-7z"
                    />
                  </svg>
                </div>
              </div>
              <div class="ml-4">
                <dt class="text-lg leading-6 font-medium text-gray-900">
                  Deney sonuclarini analiz edecek vaktin mi yok?
                </dt>
                <dd class="mt-2 text-base text-gray-500">
                  Merak etme BioHub her zaman seninle. Deneylerinin analizlerini
                  biz yapalim! Daha fazla bilgi için ürünlerimizi incele.
                </dd>
              </div>
            </div>

            <div v-html="dataLogo" class="fill text-indigo-500"></div>

            <div class="flex md:w-5/6">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
                >
                  <!-- Heroicon name: outline/annotation -->
                  <svg
                    class="h-6 w-6"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"
                    />
                  </svg>
                </div>
              </div>
              <div class="ml-4">
                <dt class="text-lg leading-6 font-medium text-gray-900">
                  Fikrini geliştirecek bir partner ya da destek alabilecegin bir
                  mentor mu ariyorsun?
                </dt>
                <dd class="mt-2 text-base text-gray-500">
                  BioHub'da sadece ihtiyaclar degil fikirler de paylasilir!
                  İster BioHub'daki diğer müşterilerimiz ile ister mentorlerimiz
                  ile gorusup onlardan fikir ve destek alabilirsin.
                </dd>
              </div>
            </div>

            <div v-html="teamworkLogo" class="w-auto"></div>
          </dl>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import cityLogo from '~/assets/city.svg?raw'
import dataLogo from '~/assets/data.svg?raw'
import bioLogo from '~/assets/bio.svg?raw'
import growthLogo from '~/assets/growth.svg?raw'
import scienceLogo from '~/assets/science.svg?raw'
import partnerLogo from '~/assets/partner.svg?raw'
import teamworkLogo from '~/assets/teamwork.svg?raw'

export default Vue.extend({
  data() {
    return {
      mobileMenu: false,
      bioLogo,
      cityLogo,
      dataLogo,
      growthLogo,
      partnerLogo,
      scienceLogo,
      teamworkLogo,
    }
  },
  methods: {
    toggle() {
      this.mobileMenu = !this.mobileMenu
    },
  },
})
</script>

<style></style>
