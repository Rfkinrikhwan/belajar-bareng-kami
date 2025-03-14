<template>
  <div class="min-h-screen bg-gradient-to-br from-teal-50 to-green-100 p-2 sm:p-4 md:p-6">
    <div class="max-w-5xl mx-auto">
      <!-- Header dengan Animasi -->
      <header
        class="text-center py-6 md:py-10 relative overflow-hidden rounded-xl bg-gradient-to-r from-teal-600 to-green-600 text-white mb-8 shadow-lg"
      >
        <div class="absolute inset-0 opacity-10">
          <div class="network-animation absolute inset-0"></div>
        </div>
        <h1 class="text-3xl md:text-4xl font-bold mb-2 relative z-10 animate-fade-in">
          Dokumentasi Jaringan & Domain
        </h1>
        <p class="text-base md:text-lg text-teal-100 animate-slide-up">
          Konsep dasar jaringan komputer dan sistem domain
        </p>
      </header>

      <!-- Main Navigation Bar -->
      <nav
        class="bg-white rounded-lg shadow-md p-3 mb-4 sticky top-2 md:top-4 z-20 overflow-x-auto"
      >
        <ul class="flex flex-wrap justify-center gap-3 md:gap-4">
          <li>
            <a
              href="/"
              class="px-3 py-1.5 md:px-4 md:py-2 rounded-md text-sm md:text-base whitespace-nowrap transition-all duration-300 transform hover:scale-105 bg-teal-600 text-white shadow-md flex items-center"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-4 w-4 mr-1"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                />
              </svg>
              Beranda
            </a>
          </li>
          <li>
            <a
              href="/html-docs"
              class="px-3 py-1.5 md:px-4 md:py-2 rounded-md text-sm md:text-base whitespace-nowrap transition-all duration-300 transform hover:scale-105 bg-indigo-600 text-white shadow-md flex items-center"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-4 w-4 mr-1"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"
                />
              </svg>
              Dokumentasi HTML
            </a>
          </li>
        </ul>
      </nav>

      <!-- Navigasi Section -->
      <nav
        class="bg-white rounded-lg shadow-md p-3 mb-6 md:mb-8 sticky top-20 md:top-24 z-10 overflow-x-auto"
      >
        <ul
          class="flex flex-nowrap md:flex-wrap justify-start md:justify-center gap-2 md:gap-4 min-w-max"
        >
          <li v-for="section in sections" :key="section.id">
            <button
              @click="activeSection = section.id"
              class="px-3 py-1.5 md:px-4 md:py-2 rounded-md text-sm md:text-base whitespace-nowrap transition-all duration-300 transform hover:scale-105"
              :class="
                activeSection === section.id
                  ? 'bg-teal-600 text-white shadow-md'
                  : 'bg-gray-100 text-gray-700 hover:bg-gray-200'
              "
            >
              {{ section.name }}
            </button>
          </li>
        </ul>
      </nav>

      <!-- Content Container -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden">
        <!-- LAN Section -->
        <div v-if="activeSection === 'lan'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-teal-700">Local Area Network (LAN)</h2>
            <p class="text-sm md:text-base text-gray-600">Jaringan komputer dalam area terbatas</p>
            <div class="h-1 w-20 bg-teal-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <!-- LAN Definition -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Pengertian LAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base mb-4">
                      <strong>Local Area Network (LAN)</strong> adalah jaringan komputer yang
                      mencakup area geografis yang relatif kecil, seperti rumah, kantor, atau
                      gedung. LAN biasanya dikelola oleh satu organisasi atau individu.
                    </p>
                    <p class="text-gray-800 text-sm md:text-base">
                      LAN memungkinkan perangkat untuk berbagi sumber daya seperti printer, file,
                      dan koneksi internet. Jaringan ini biasanya memiliki kecepatan transfer data
                      yang tinggi dan latensi rendah.
                    </p>
                  </div>
                </div>
              </div>

              <!-- LAN Characteristics -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Karakteristik LAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base space-y-2">
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Cakupan geografis terbatas (biasanya dalam satu gedung)
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Kecepatan transfer data tinggi (10 Mbps hingga 10 Gbps)
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Latensi rendah
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Dikelola oleh satu organisasi
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Biasanya menggunakan teknologi Ethernet atau Wi-Fi
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Memungkinkan berbagi sumber daya (printer, file, dll)
                      </li>
                    </ul>
                  </div>
                </div>
              </div>

              <!-- LAN Topology -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 md:col-span-2"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Topologi LAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div
                      class="text-center p-4 border border-gray-200 rounded-lg hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="topology-star mx-auto mb-3 w-24 h-24 relative">
                        <div class="absolute inset-0 flex items-center justify-center">
                          <div class="w-6 h-6 bg-teal-500 rounded-full z-10"></div>
                        </div>
                        <div
                          class="absolute top-0 left-1/2 transform -translate-x-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute top-1/4 right-0 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute bottom-1/4 right-0 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute bottom-1/4 left-0 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div class="absolute top-1/4 left-0 w-3 h-3 bg-teal-400 rounded-full"></div>
                        <!-- Lines -->
                        <div
                          class="absolute top-0 left-1/2 transform -translate-x-1/2 w-px h-10 bg-teal-300"
                        ></div>
                        <div class="absolute top-1/4 right-0 w-10 h-px bg-teal-300"></div>
                        <div class="absolute bottom-1/4 right-0 w-10 h-px bg-teal-300"></div>
                        <div
                          class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-px h-10 bg-teal-300"
                        ></div>
                        <div class="absolute bottom-1/4 left-0 w-10 h-px bg-teal-300"></div>
                        <div class="absolute top-1/4 left-0 w-10 h-px bg-teal-300"></div>
                      </div>
                      <h4 class="font-semibold text-teal-700">Topologi Star</h4>
                      <p class="text-sm text-gray-600 mt-2">
                        Semua perangkat terhubung ke satu titik pusat (switch/hub)
                      </p>
                    </div>

                    <div
                      class="text-center p-4 border border-gray-200 rounded-lg hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="topology-bus mx-auto mb-3 w-24 h-24 relative">
                        <div
                          class="absolute left-0 right-0 top-1/2 transform -translate-y-1/2 h-1 bg-teal-500"
                        ></div>
                        <div
                          class="absolute left-1/6 top-1/2 transform -translate-y-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute left-2/6 top-1/2 transform -translate-y-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute left-3/6 top-1/2 transform -translate-y-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute left-4/6 top-1/2 transform -translate-y-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute left-5/6 top-1/2 transform -translate-y-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <!-- Lines -->
                        <div
                          class="absolute left-1/6 top-1/2 transform -translate-y-1/2 w-px h-6 bg-teal-300"
                        ></div>
                        <div
                          class="absolute left-2/6 top-1/2 transform -translate-y-1/2 w-px h-6 bg-teal-300"
                        ></div>
                        <div
                          class="absolute left-3/6 top-1/2 transform -translate-y-1/2 w-px h-6 bg-teal-300"
                        ></div>
                        <div
                          class="absolute left-4/6 top-1/2 transform -translate-y-1/2 w-px h-6 bg-teal-300"
                        ></div>
                        <div
                          class="absolute left-5/6 top-1/2 transform -translate-y-1/2 w-px h-6 bg-teal-300"
                        ></div>
                      </div>
                      <h4 class="font-semibold text-teal-700">Topologi Bus</h4>
                      <p class="text-sm text-gray-600 mt-2">
                        Semua perangkat terhubung ke satu kabel utama
                      </p>
                    </div>

                    <div
                      class="text-center p-4 border border-gray-200 rounded-lg hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="topology-ring mx-auto mb-3 w-24 h-24 relative">
                        <div class="absolute inset-2 border-4 border-teal-500 rounded-full"></div>
                        <div
                          class="absolute top-0 left-1/2 transform -translate-x-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute top-1/4 right-0 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute bottom-1/4 right-0 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div
                          class="absolute bottom-1/4 left-0 w-3 h-3 bg-teal-400 rounded-full"
                        ></div>
                        <div class="absolute top-1/4 left-0 w-3 h-3 bg-teal-400 rounded-full"></div>
                      </div>
                      <h4 class="font-semibold text-teal-700">Topologi Ring</h4>
                      <p class="text-sm text-gray-600 mt-2">
                        Perangkat terhubung dalam bentuk lingkaran tertutup
                      </p>
                    </div>
                  </div>
                </div>
              </div>

              <!-- LAN Example -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 md:col-span-2"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Contoh Implementasi LAN
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div
                    class="lan-example relative h-64 md:h-80 border border-gray-200 rounded-lg overflow-hidden bg-gray-50"
                  >
                    <div
                      class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-16 h-16 bg-teal-100 rounded-lg flex items-center justify-center border border-teal-300"
                    >
                      <div class="text-teal-600 font-bold text-xs">Router</div>
                    </div>

                    <div
                      class="absolute top-1/4 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center border border-blue-300"
                    >
                      <div class="text-blue-600 font-bold text-xs">Switch</div>
                    </div>

                    <!-- Computers -->
                    <div
                      class="absolute top-1/6 left-1/4 transform -translate-x-1/2 -translate-y-1/2 w-10 h-10 bg-gray-100 rounded flex items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 text-xs">PC1</div>
                    </div>

                    <div
                      class="absolute top-1/6 left-3/4 transform -translate-x-1/2 -translate-y-1/2 w-10 h-10 bg-gray-100 rounded flex items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 text-xs">PC2</div>
                    </div>

                    <div
                      class="absolute bottom-1/6 left-1/4 transform -translate-x-1/2 -translate-y-1/2 w-10 h-10 bg-gray-100 rounded flex items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 text-xs">PC3</div>
                    </div>

                    <div
                      class="absolute bottom-1/6 left-3/4 transform -translate-x-1/2 -translate-y-1/2 w-10 h-10 bg-gray-100 rounded flex items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 text-xs">PC4</div>
                    </div>

                    <!-- Printer -->
                    <div
                      class="absolute bottom-1/4 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-10 h-10 bg-green-100 rounded flex items-center justify-center border border-green-300"
                    >
                      <div class="text-green-600 text-xs">Printer</div>
                    </div>

                    <!-- Lines -->
                    <div class="absolute top-1/4 left-1/2 w-px h-12 bg-teal-400"></div>
                    <div class="absolute top-1/6 left-1/4 w-px h-8 bg-blue-400"></div>
                    <div class="absolute top-1/6 left-3/4 w-px h-8 bg-blue-400"></div>
                    <div class="absolute bottom-1/6 left-1/4 w-px h-24 bg-blue-400"></div>
                    <div class="absolute bottom-1/6 left-3/4 w-px h-24 bg-blue-400"></div>
                    <div class="absolute bottom-1/4 left-1/2 w-px h-12 bg-blue-400"></div>

                    <div class="absolute top-1/4 left-1/4 w-32 h-px bg-blue-400"></div>
                    <div class="absolute top-1/4 right-1/4 w-32 h-px bg-blue-400"></div>

                    <div
                      class="absolute top-1/2 left-1/2 transform -translate-y-1/2 w-px h-16 bg-teal-500"
                    ></div>
                    <div
                      class="absolute top-1/2 left-1/2 transform -translate-x-1/2 w-16 h-px bg-teal-500"
                    ></div>

                    <div
                      class="absolute bottom-0 left-0 right-0 p-2 bg-teal-600 text-white text-xs text-center"
                    >
                      Contoh LAN di Kantor Kecil
                    </div>
                  </div>
                  <p class="text-sm text-gray-600 mt-4 text-center">
                    Ilustrasi sederhana jaringan LAN dengan router, switch, komputer, dan printer
                    yang saling terhubung.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- WAN Section -->
        <div v-if="activeSection === 'wan'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-teal-700">Wide Area Network (WAN)</h2>
            <p class="text-sm md:text-base text-gray-600">
              Jaringan komputer yang mencakup area geografis yang luas
            </p>
            <div class="h-1 w-20 bg-teal-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <!-- WAN Definition -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Pengertian WAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base mb-4">
                      <strong>Wide Area Network (WAN)</strong> adalah jaringan komputer yang
                      mencakup area geografis yang luas, seperti kota, negara, atau bahkan benua.
                      WAN menghubungkan beberapa LAN yang terpisah secara geografis.
                    </p>
                    <p class="text-gray-800 text-sm md:text-base">
                      Internet adalah contoh terbesar dari WAN. WAN biasanya menggunakan teknologi
                      seperti leased line, satelit, atau koneksi fiber optik untuk menghubungkan
                      jaringan yang berjauhan.
                    </p>
                  </div>
                </div>
              </div>

              <!-- WAN Characteristics -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Karakteristik WAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base space-y-2">
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Cakupan geografis luas (antar kota, negara, benua)
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Kecepatan transfer data lebih rendah dibanding LAN
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Latensi lebih tinggi
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Biasanya dikelola oleh beberapa organisasi atau penyedia layanan
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Menggunakan teknologi seperti leased line, MPLS, satelit
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Memerlukan router untuk menghubungkan jaringan yang berbeda
                      </li>
                    </ul>
                  </div>
                </div>
              </div>

              <!-- WAN Example -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 md:col-span-2"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Contoh Implementasi WAN
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div
                    class="wan-example relative h-64 md:h-80 border border-gray-200 rounded-lg overflow-hidden bg-gray-50"
                  >
                    <!-- Cloud/Internet -->
                    <div
                      class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-24 h-16 bg-blue-100 rounded-full flex items-center justify-center border border-blue-300"
                    >
                      <div class="text-blue-600 font-bold text-xs">Internet</div>
                    </div>

                    <!-- Office 1 (Jakarta) -->
                    <div
                      class="absolute top-1/4 left-1/4 transform -translate-x-1/2 -translate-y-1/2 w-20 h-16 bg-teal-100 rounded-lg flex flex-col items-center justify-center border border-teal-300"
                    >
                      <div class="text-teal-600 font-bold text-xs">Kantor Jakarta</div>
                      <div class="text-teal-500 text-xs">LAN</div>
                    </div>

                    <!-- Office 2 (Surabaya) -->
                    <div
                      class="absolute top-1/4 right-1/4 transform translate-x-1/2 -translate-y-1/2 w-20 h-16 bg-teal-100 rounded-lg flex flex-col items-center justify-center border border-teal-300"
                    >
                      <div class="text-teal-600 font-bold text-xs">Kantor Surabaya</div>
                      <div class="text-teal-500 text-xs">LAN</div>
                    </div>

                    <!-- Office 3 (Singapore) -->
                    <div
                      class="absolute bottom-1/4 left-1/4 transform -translate-x-1/2 translate-y-1/2 w-20 h-16 bg-teal-100 rounded-lg flex flex-col items-center justify-center border border-teal-300"
                    >
                      <div class="text-teal-600 font-bold text-xs">Kantor Singapura</div>
                      <div class="text-teal-500 text-xs">LAN</div>
                    </div>

                    <!-- Office 4 (New York) -->
                    <div
                      class="absolute bottom-1/4 right-1/4 transform translate-x-1/2 translate-y-1/2 w-20 h-16 bg-teal-100 rounded-lg flex flex-col items-center justify-center border border-teal-300"
                    >
                      <div class="text-teal-600 font-bold text-xs">Kantor New York</div>
                      <div class="text-teal-500 text-xs">LAN</div>
                    </div>

                    <!-- Lines -->
                    <div
                      class="absolute top-1/4 left-1/4 w-24 h-24 border-t-2 border-r-2 border-blue-400 rounded-tr-full"
                    ></div>
                    <div
                      class="absolute top-1/4 right-1/4 w-24 h-24 border-t-2 border-l-2 border-blue-400 rounded-tl-full"
                    ></div>
                    <div
                      class="absolute bottom-1/4 left-1/4 w-24 h-24 border-b-2 border-r-2 border-blue-400 rounded-br-full"
                    ></div>
                    <div
                      class="absolute bottom-1/4 right-1/4 w-24 h-24 border-b-2 border-l-2 border-blue-400 rounded-bl-full"
                    ></div>

                    <div
                      class="absolute bottom-0 left-0 right-0 p-2 bg-teal-600 text-white text-xs text-center"
                    >
                      Contoh WAN Perusahaan Multinasional
                    </div>
                  </div>
                  <p class="text-sm text-gray-600 mt-4 text-center">
                    Ilustrasi jaringan WAN yang menghubungkan kantor-kantor di berbagai lokasi
                    geografis melalui internet.
                  </p>
                </div>
              </div>

              <!-- WAN vs LAN -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 md:col-span-2"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Perbandingan WAN vs LAN
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="overflow-x-auto">
                    <table class="min-w-full border-collapse border border-gray-300 text-sm">
                      <thead>
                        <tr class="bg-teal-100">
                          <th class="border border-gray-300 p-2 md:p-3 text-left">Aspek</th>
                          <th class="border border-gray-300 p-2 md:p-3 text-left">LAN</th>
                          <th class="border border-gray-300 p-2 md:p-3 text-left">WAN</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">
                            Cakupan Area
                          </td>
                          <td class="border border-gray-300 p-2 md:p-3">
                            Terbatas (gedung, kampus)
                          </td>
                          <td class="border border-gray-300 p-2 md:p-3">
                            Luas (antar kota, negara)
                          </td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Kecepatan</td>
                          <td class="border border-gray-300 p-2 md:p-3">
                            Tinggi (10 Mbps - 10 Gbps)
                          </td>
                          <td class="border border-gray-300 p-2 md:p-3">
                            Bervariasi (56 Kbps - 100+ Mbps)
                          </td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Latensi</td>
                          <td class="border border-gray-300 p-2 md:p-3">Rendah</td>
                          <td class="border border-gray-300 p-2 md:p-3">Tinggi</td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Kepemilikan</td>
                          <td class="border border-gray-300 p-2 md:p-3">Satu organisasi</td>
                          <td class="border border-gray-300 p-2 md:p-3">
                            Beberapa organisasi/penyedia
                          </td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Biaya</td>
                          <td class="border border-gray-300 p-2 md:p-3">Relatif rendah</td>
                          <td class="border border-gray-300 p-2 md:p-3">Relatif tinggi</td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- MAN Section -->
        <div v-if="activeSection === 'man'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-teal-700">
              Metropolitan Area Network (MAN)
            </h2>
            <p class="text-sm md:text-base text-gray-600">Jaringan komputer dalam skala kota</p>
            <div class="h-1 w-20 bg-teal-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <!-- MAN Definition -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Pengertian MAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base mb-4">
                      <strong>Metropolitan Area Network (MAN)</strong> adalah jaringan komputer yang
                      mencakup area geografis sebesar kota atau metropolitan. MAN menghubungkan
                      beberapa LAN dalam satu kota.
                    </p>
                    <p class="text-gray-800 text-sm md:text-base">
                      MAN biasanya dikelola oleh satu organisasi atau konsorsium, seperti pemerintah
                      kota, perusahaan telekomunikasi, atau institusi pendidikan. MAN menjembatani
                      antara LAN dan WAN dalam hal cakupan area.
                    </p>
                  </div>
                </div>
              </div>

              <!-- MAN Characteristics -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Karakteristik MAN</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base space-y-2">
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Cakupan geografis menengah (satu kota)
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Kecepatan transfer data menengah (antara LAN dan WAN)
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Biasanya menggunakan teknologi seperti fiber optik
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Sering digunakan untuk menghubungkan kantor cabang dalam satu kota
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Contoh: jaringan TV kabel, jaringan kampus universitas
                      </li>
                      <li class="hover:text-teal-600 transition-colors duration-300">
                        Lebih ekonomis daripada WAN untuk area kota
                      </li>
                    </ul>
                  </div>
                </div>
              </div>

              <!-- MAN Example -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 md:col-span-2"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Contoh Implementasi MAN
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div
                    class="man-example relative h-64 md:h-80 border border-gray-200 rounded-lg overflow-hidden bg-gray-50"
                  >
                    <!-- City Center -->
                    <div
                      class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-20 h-20 bg-teal-100 rounded-full flex items-center justify-center border border-teal-300"
                    >
                      <div class="text-teal-600 font-bold text-xs text-center">Pusat Data Kota</div>
                    </div>

                    <!-- Buildings -->
                    <div
                      class="absolute top-1/6 left-1/4 transform -translate-x-1/2 -translate-y-1/2 w-16 h-12 bg-gray-200 rounded flex flex-col items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 font-bold text-xs">Kantor Walikota</div>
                      <div class="text-gray-500 text-xs">LAN</div>
                    </div>

                    <div
                      class="absolute top-1/6 right-1/4 transform translate-x-1/2 -translate-y-1/2 w-16 h-12 bg-gray-200 rounded flex flex-col items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 font-bold text-xs">Universitas</div>
                      <div class="text-gray-500 text-xs">LAN</div>
                    </div>

                    <div
                      class="absolute bottom-1/6 left-1/4 transform -translate-x-1/2 translate-y-1/2 w-16 h-12 bg-gray-200 rounded flex flex-col items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 font-bold text-xs">Rumah Sakit</div>
                      <div class="text-gray-500 text-xs">LAN</div>
                    </div>

                    <div
                      class="absolute bottom-1/6 right-1/4 transform translate-x-1/2 translate-y-1/2 w-16 h-12 bg-gray-200 rounded flex flex-col items-center justify-center border border-gray-300"
                    >
                      <div class="text-gray-600 font-bold text-xs">Perpustakaan</div>
                      <div class="text-gray-500 text-xs">LAN</div>
                    </div>

                    <!-- Lines -->
                    <div
                      class="absolute top-1/4 left-1/3 w-1/3 h-1/4 border-t-2 border-l-2 border-teal-400 rounded-tl-full"
                    ></div>
                    <div
                      class="absolute top-1/4 right-1/3 w-1/3 h-1/4 border-t-2 border-r-2 border-teal-400 rounded-tr-full"
                    ></div>
                    <div
                      class="absolute bottom-1/4 left-1/3 w-1/3 h-1/4 border-b-2 border-l-2 border-teal-400 rounded-bl-full"
                    ></div>
                    <div
                      class="absolute bottom-1/4 right-1/3 w-1/3 h-1/4 border-b-2 border-r-2 border-teal-400 rounded-br-full"
                    ></div>

                    <div
                      class="absolute bottom-0 left-0 right-0 p-2 bg-teal-600 text-white text-xs text-center"
                    >
                      Contoh MAN Pemerintah Kota
                    </div>
                  </div>
                  <p class="text-sm text-gray-600 mt-4 text-center">
                    Ilustrasi jaringan MAN yang menghubungkan berbagai institusi pemerintah dan
                    publik dalam satu kota.
                  </p>
                </div>
              </div>

              <!-- Comparison -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 md:col-span-2"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Perbandingan LAN, MAN, dan WAN
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="overflow-x-auto">
                    <table class="min-w-full border-collapse border border-gray-300 text-sm">
                      <thead>
                        <tr class="bg-teal-100">
                          <th class="border border-gray-300 p-2 md:p-3 text-left">Aspek</th>
                          <th class="border border-gray-300 p-2 md:p-3 text-left">LAN</th>
                          <th class="border border-gray-300 p-2 md:p-3 text-left">MAN</th>
                          <th class="border border-gray-300 p-2 md:p-3 text-left">WAN</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">
                            Cakupan Area
                          </td>
                          <td class="border border-gray-300 p-2 md:p-3">Gedung/Kampus</td>
                          <td class="border border-gray-300 p-2 md:p-3">Kota</td>
                          <td class="border border-gray-300 p-2 md:p-3">Antar kota/negara</td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Jarak</td>
                          <td class="border border-gray-300 p-2 md:p-3">Hingga 1-2 km</td>
                          <td class="border border-gray-300 p-2 md:p-3">5-50 km</td>
                          <td class="border border-gray-300 p-2 md:p-3">100+ km</td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Kecepatan</td>
                          <td class="border border-gray-300 p-2 md:p-3">Tinggi</td>
                          <td class="border border-gray-300 p-2 md:p-3">Menengah-Tinggi</td>
                          <td class="border border-gray-300 p-2 md:p-3">Bervariasi</td>
                        </tr>
                        <tr class="hover:bg-gray-50 transition-colors">
                          <td class="border border-gray-300 p-2 md:p-3 font-medium">Kepemilikan</td>
                          <td class="border border-gray-300 p-2 md:p-3">Pribadi</td>
                          <td class="border border-gray-300 p-2 md:p-3">Pribadi/Publik</td>
                          <td class="border border-gray-300 p-2 md:p-3">Publik/Penyedia</td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Domain Section -->
        <div v-if="activeSection === 'domain'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-teal-700">Domain</h2>
            <p class="text-sm md:text-base text-gray-600">Pengertian dan jenis-jenis domain</p>
            <div class="h-1 w-20 bg-teal-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-6">
              <!-- Domain Definition -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Pengertian Domain</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base mb-4">
                      <strong>Domain</strong> adalah nama unik yang mengidentifikasi sebuah situs
                      web di internet. Domain berfungsi sebagai alamat yang memudahkan pengguna
                      untuk mengakses situs web tanpa harus mengingat alamat IP numerik.
                    </p>
                    <p class="text-gray-800 text-sm md:text-base">
                      Sistem Domain Name System (DNS) menerjemahkan nama domain yang mudah diingat
                      (seperti example.com) menjadi alamat IP numerik (seperti 192.168.1.1) yang
                      digunakan komputer untuk berkomunikasi satu sama lain.
                    </p>
                  </div>
                </div>
              </div>

              <!-- Domain Structure -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Struktur Domain</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div
                    class="domain-structure relative p-4 border border-gray-200 rounded-lg bg-gray-50 mb-4"
                  >
                    <div
                      class="flex flex-col md:flex-row items-center justify-center gap-2 md:gap-4"
                    >
                      <div
                        class="domain-part p-2 bg-green-100 border border-green-300 rounded text-center min-w-[100px]"
                      >
                        <div class="text-green-700 font-bold">blog</div>
                        <div class="text-xs text-green-600">Subdomain</div>
                      </div>
                      <div class="text-gray-400">.</div>
                      <div
                        class="domain-part p-2 bg-teal-100 border border-teal-300 rounded text-center min-w-[100px]"
                      >
                        <div class="text-teal-700 font-bold">example</div>
                        <div class="text-xs text-teal-600">Second-level Domain</div>
                      </div>
                      <div class="text-gray-400">.</div>
                      <div
                        class="domain-part p-2 bg-blue-100 border border-blue-300 rounded text-center min-w-[100px]"
                      >
                        <div class="text-blue-700 font-bold">com</div>
                        <div class="text-xs text-blue-600">Top-level Domain (TLD)</div>
                      </div>
                    </div>
                  </div>
                  <p class="text-gray-800 text-sm md:text-base">
                    Nama domain terdiri dari beberapa bagian yang dipisahkan oleh titik:
                  </p>
                  <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base mt-2 space-y-2">
                    <li>
                      <strong>Top-level Domain (TLD)</strong>: Bagian paling kanan (.com, .org,
                      .net)
                    </li>
                    <li>
                      <strong>Second-level Domain</strong>: Nama utama yang dipilih oleh pemilik
                      (example)
                    </li>
                    <li><strong>Subdomain</strong>: Bagian opsional di sebelah kiri (blog, www)</li>
                  </ul>
                </div>
              </div>

              <!-- Domain Types -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Jenis-jenis Domain (TLD)
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <!-- Generic TLDs -->
                    <div class="p-4 border border-gray-200 rounded-lg bg-gray-50">
                      <h4 class="font-semibold text-teal-700 mb-2">Generic TLDs (gTLD)</h4>
                      <p class="text-sm text-gray-600 mb-3">
                        Domain umum yang tidak terikat dengan negara tertentu
                      </p>
                      <div class="space-y-2">
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.com</div>
                          <div class="text-sm">Commercial - untuk bisnis dan komersial</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.org</div>
                          <div class="text-sm">Organization - untuk organisasi non-profit</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.net</div>
                          <div class="text-sm">Network - awalnya untuk layanan jaringan</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.edu</div>
                          <div class="text-sm">Education - untuk institusi pendidikan</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.gov</div>
                          <div class="text-sm">Government - untuk lembaga pemerintah</div>
                        </div>
                      </div>
                    </div>

                    <!-- Country Code TLDs -->
                    <div class="p-4 border border-gray-200 rounded-lg bg-gray-50">
                      <h4 class="font-semibold text-teal-700 mb-2">Country Code TLDs (ccTLD)</h4>
                      <p class="text-sm text-gray-600 mb-3">
                        Domain yang terkait dengan negara tertentu
                      </p>
                      <div class="space-y-2">
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.id</div>
                          <div class="text-sm">Indonesia</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.us</div>
                          <div class="text-sm">United States</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.uk</div>
                          <div class="text-sm">United Kingdom</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.jp</div>
                          <div class="text-sm">Japan</div>
                        </div>
                        <div
                          class="flex items-center p-2 bg-white rounded border border-gray-200 hover:bg-teal-50 transition-colors duration-300"
                        >
                          <div class="w-16 font-bold text-teal-600">.au</div>
                          <div class="text-sm">Australia</div>
                        </div>
                      </div>
                    </div>
                  </div>

                  <!-- New TLDs -->
                  <div class="mt-4 p-4 border border-gray-200 rounded-lg bg-gray-50">
                    <h4 class="font-semibold text-teal-700 mb-2">New gTLDs</h4>
                    <p class="text-sm text-gray-600 mb-3">
                      Domain baru yang lebih spesifik untuk industri atau keperluan tertentu
                    </p>
                    <div class="flex flex-wrap gap-2">
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.app</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.blog</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.shop</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.tech</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.store</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.online</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.io</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.ai</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.dev</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.design</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.cloud</span
                      >
                      <span
                        class="px-3 py-1 bg-white rounded-full border border-gray-200 text-sm hover:bg-teal-50 transition-colors duration-300"
                        >.agency</span
                      >
                    </div>
                  </div>
                </div>
              </div>

              <!-- Domain Examples -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Contoh Domain dan Penjelasannya
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="space-y-4">
                    <div
                      class="p-4 border border-gray-200 rounded-lg hover:bg-gray-50 transition-colors duration-300"
                    >
                      <div class="flex flex-col md:flex-row md:items-center gap-2 md:gap-4">
                        <div class="font-bold text-teal-700 text-lg md:w-1/3">google.com</div>
                        <div class="md:w-2/3">
                          <p class="text-sm md:text-base text-gray-700">
                            Domain untuk mesin pencari Google. Menggunakan TLD .com yang menunjukkan
                            sifat komersial. Google adalah nama perusahaan yang menjadi second-level
                            domain.
                          </p>
                        </div>
                      </div>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg hover:bg-gray-50 transition-colors duration-300"
                    >
                      <div class="flex flex-col md:flex-row md:items-center gap-2 md:gap-4">
                        <div class="font-bold text-teal-700 text-lg md:w-1/3">wikipedia.org</div>
                        <div class="md:w-2/3">
                          <p class="text-sm md:text-base text-gray-700">
                            Domain untuk ensiklopedia online Wikipedia. Menggunakan TLD .org yang
                            menunjukkan sifat non-profit. Wikipedia adalah nama proyek yang menjadi
                            second-level domain.
                          </p>
                        </div>
                      </div>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg hover:bg-gray-50 transition-colors duration-300"
                    >
                      <div class="flex flex-col md:flex-row md:items-center gap-2 md:gap-4">
                        <div class="font-bold text-teal-700 text-lg md:w-1/3">mail.yahoo.com</div>
                        <div class="md:w-2/3">
                          <p class="text-sm md:text-base text-gray-700">
                            Domain untuk layanan email Yahoo. "mail" adalah subdomain, "yahoo"
                            adalah second-level domain, dan ".com" adalah TLD. Subdomain "mail"
                            menunjukkan layanan spesifik (email) dari Yahoo.
                          </p>
                        </div>
                      </div>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg hover:bg-gray-50 transition-colors duration-300"
                    >
                      <div class="flex flex-col md:flex-row md:items-center gap-2 md:gap-4">
                        <div class="font-bold text-teal-700 text-lg md:w-1/3">harvard.edu</div>
                        <div class="md:w-2/3">
                          <p class="text-sm md:text-base text-gray-700">
                            Domain untuk Universitas Harvard. Menggunakan TLD .edu yang khusus untuk
                            institusi pendidikan. Harvard adalah nama universitas yang menjadi
                            second-level domain.
                          </p>
                        </div>
                      </div>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg hover:bg-gray-50 transition-colors duration-300"
                    >
                      <div class="flex flex-col md:flex-row md:items-center gap-2 md:gap-4">
                        <div class="font-bold text-teal-700 text-lg md:w-1/3">detik.com</div>
                        <div class="md:w-2/3">
                          <p class="text-sm md:text-base text-gray-700">
                            Domain untuk portal berita Indonesia. Menggunakan TLD .com untuk situs
                            komersial. Detik adalah nama perusahaan media yang menjadi second-level
                            domain.
                          </p>
                        </div>
                      </div>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg hover:bg-gray-50 transition-colors duration-300"
                    >
                      <div class="flex flex-col md:flex-row md:items-center gap-2 md:gap-4">
                        <div class="font-bold text-teal-700 text-lg md:w-1/3">go.id</div>
                        <div class="md:w-2/3">
                          <p class="text-sm md:text-base text-gray-700">
                            Domain untuk situs pemerintah Indonesia. Menggunakan ccTLD .id
                            (Indonesia) dengan second-level domain "go" yang menunjukkan government
                            (pemerintah).
                          </p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Hosting Section -->
        <div v-if="activeSection === 'hosting'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-teal-700">Hosting</h2>
            <p class="text-sm md:text-base text-gray-600">Pengertian dan jenis-jenis hosting</p>
            <div class="h-1 w-20 bg-teal-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-6">
              <!-- Hosting Definition -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">Pengertian Hosting</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base mb-4">
                      <strong>Web Hosting</strong> adalah layanan yang menyediakan ruang penyimpanan
                      dan akses untuk situs web di internet. Hosting menyimpan semua file, gambar,
                      dan database yang diperlukan untuk menjalankan situs web, sehingga dapat
                      diakses oleh pengunjung melalui internet.
                    </p>
                    <p class="text-gray-800 text-sm md:text-base">
                      Penyedia hosting mengoperasikan server yang terhubung ke internet dengan
                      kecepatan tinggi, memastikan situs web dapat diakses 24/7. Hosting berbeda
                      dengan domain, di mana domain adalah alamat situs web, sedangkan hosting
                      adalah tempat penyimpanan konten situs web.
                    </p>
                  </div>
                </div>
              </div>

              <!-- Hosting Types -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Jenis-jenis Hosting
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <!-- Shared Hosting -->
                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="flex items-center mb-2">
                        <div
                          class="w-10 h-10 bg-teal-100 rounded-full flex items-center justify-center mr-3"
                        >
                          <div class="text-teal-600 font-bold">1</div>
                        </div>
                        <h4 class="font-semibold text-teal-700">Shared Hosting</h4>
                      </div>
                      <p class="text-sm text-gray-600 mb-2">
                        Hosting di mana satu server fisik dibagi untuk banyak situs web. Paling
                        ekonomis tapi sumber daya terbatas.
                      </p>
                      <div class="text-xs text-gray-500">
                        Cocok untuk: Blog pribadi, situs bisnis kecil, portofolio
                      </div>
                    </div>

                    <!-- VPS Hosting -->
                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="flex items-center mb-2">
                        <div
                          class="w-10 h-10 bg-teal-100 rounded-full flex items-center justify-center mr-3"
                        >
                          <div class="text-teal-600 font-bold">2</div>
                        </div>
                        <h4 class="font-semibold text-teal-700">VPS Hosting</h4>
                      </div>
                      <p class="text-sm text-gray-600 mb-2">
                        Virtual Private Server - satu server fisik dibagi menjadi beberapa server
                        virtual dengan sumber daya terjamin.
                      </p>
                      <div class="text-xs text-gray-500">
                        Cocok untuk: Situs dengan traffic menengah, aplikasi web, e-commerce kecil
                      </div>
                    </div>

                    <!-- Dedicated Hosting -->
                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="flex items-center mb-2">
                        <div
                          class="w-10 h-10 bg-teal-100 rounded-full flex items-center justify-center mr-3"
                        >
                          <div class="text-teal-600 font-bold">3</div>
                        </div>
                        <h4 class="font-semibold text-teal-700">Dedicated Hosting</h4>
                      </div>
                      <p class="text-sm text-gray-600 mb-2">
                        Satu server fisik penuh didedikasikan untuk satu situs web. Performa
                        maksimal tapi biaya tinggi.
                      </p>
                      <div class="text-xs text-gray-500">
                        Cocok untuk: Situs dengan traffic tinggi, aplikasi kompleks, e-commerce
                        besar
                      </div>
                    </div>

                    <!-- Cloud Hosting -->
                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="flex items-center mb-2">
                        <div
                          class="w-10 h-10 bg-teal-100 rounded-full flex items-center justify-center mr-3"
                        >
                          <div class="text-teal-600 font-bold">4</div>
                        </div>
                        <h4 class="font-semibold text-teal-700">Cloud Hosting</h4>
                      </div>
                      <p class="text-sm text-gray-600 mb-2">
                        Hosting yang menggunakan jaringan server terdistribusi. Skalabel dan
                        fleksibel sesuai kebutuhan.
                      </p>
                      <div class="text-xs text-gray-500">
                        Cocok untuk: Situs dengan traffic fluktuatif, aplikasi SaaS, startup
                      </div>
                    </div>

                    <!-- Managed WordPress Hosting -->
                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300 md:col-span-2"
                    >
                      <div class="flex items-center mb-2">
                        <div
                          class="w-10 h-10 bg-teal-100 rounded-full flex items-center justify-center mr-3"
                        >
                          <div class="text-teal-600 font-bold">5</div>
                        </div>
                        <h4 class="font-semibold text-teal-700">Managed WordPress Hosting</h4>
                      </div>
                      <p class="text-sm text-gray-600 mb-2">
                        Hosting yang dioptimalkan khusus untuk WordPress. Termasuk pemeliharaan,
                        keamanan, dan performa yang dioptimalkan.
                      </p>
                      <div class="text-xs text-gray-500">
                        Cocok untuk: Blog WordPress, situs bisnis berbasis WordPress
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Hosting vs Domain -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Perbedaan Hosting dan Domain
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div
                    class="hosting-domain-comparison relative p-4 border border-gray-200 rounded-lg bg-gray-50 mb-4"
                  >
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                      <div class="p-4 bg-white rounded-lg border border-teal-200 shadow-sm">
                        <h4 class="font-semibold text-teal-700 mb-2 text-center">Domain</h4>
                        <div class="space-y-2">
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">
                              Alamat situs web di internet (contoh: example.com)
                            </p>
                          </div>
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">
                              Seperti alamat rumah yang memudahkan orang menemukan lokasi
                            </p>
                          </div>
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">Didaftarkan melalui registrar domain</p>
                          </div>
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">Biaya tahunan untuk mempertahankan kepemilikan</p>
                          </div>
                        </div>
                      </div>

                      <div class="p-4 bg-white rounded-lg border border-teal-200 shadow-sm">
                        <h4 class="font-semibold text-teal-700 mb-2 text-center">Hosting</h4>
                        <div class="space-y-2">
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">Ruang penyimpanan untuk file situs web</p>
                          </div>
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">
                              Seperti bangunan fisik tempat konten situs web disimpan
                            </p>
                          </div>
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">Disewa dari penyedia hosting</p>
                          </div>
                          <div class="flex items-start">
                            <div
                              class="w-6 h-6 bg-teal-100 rounded-full flex items-center justify-center mr-2 mt-0.5 flex-shrink-0"
                            >
                              <div class="text-teal-600 font-bold text-xs">✓</div>
                            </div>
                            <p class="text-sm">Biaya bulanan/tahunan berdasarkan sumber daya</p>
                          </div>
                        </div>
                      </div>
                    </div>

                    <div class="mt-4 text-center text-sm text-gray-600">
                      <p>
                        Untuk membuat situs web yang berfungsi, Anda memerlukan
                        <strong>keduanya</strong>: domain sebagai alamat dan hosting sebagai tempat
                        penyimpanan.
                      </p>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Hosting Considerations -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-teal-50">
                  <h3 class="font-medium text-teal-700 text-sm md:text-base">
                    Pertimbangan Memilih Hosting
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="text-center mb-3">
                        <div
                          class="w-12 h-12 bg-teal-100 rounded-full flex items-center justify-center mx-auto"
                        >
                          <div class="text-teal-600 font-bold text-xl">⚡</div>
                        </div>
                        <h4 class="font-semibold text-teal-700 mt-2">Performa</h4>
                      </div>
                      <ul class="text-sm space-y-2 text-gray-600">
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Kecepatan loading</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Uptime (ketersediaan)</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Lokasi server</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Spesifikasi hardware</span>
                        </li>
                      </ul>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="text-center mb-3">
                        <div
                          class="w-12 h-12 bg-teal-100 rounded-full flex items-center justify-center mx-auto"
                        >
                          <div class="text-teal-600 font-bold text-xl">🔒</div>
                        </div>
                        <h4 class="font-semibold text-teal-700 mt-2">Keamanan</h4>
                      </div>
                      <ul class="text-sm space-y-2 text-gray-600">
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>SSL/TLS gratis</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Firewall</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Backup otomatis</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Proteksi DDoS</span>
                        </li>
                      </ul>
                    </div>

                    <div
                      class="p-4 border border-gray-200 rounded-lg bg-gray-50 hover:bg-teal-50 transition-colors duration-300"
                    >
                      <div class="text-center mb-3">
                        <div
                          class="w-12 h-12 bg-teal-100 rounded-full flex items-center justify-center mx-auto"
                        >
                          <div class="text-teal-600 font-bold text-xl">💰</div>
                        </div>
                        <h4 class="font-semibold text-teal-700 mt-2">Biaya & Dukungan</h4>
                      </div>
                      <ul class="text-sm space-y-2 text-gray-600">
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Harga & paket</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Dukungan 24/7</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Kebijakan refund</span>
                        </li>
                        <li class="flex items-start">
                          <span class="text-teal-500 mr-1">•</span>
                          <span>Skalabilitas</span>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Back to Top Button -->
        <button
          @click="scrollToTop"
          class="fixed bottom-6 right-6 bg-teal-600 text-white p-3 rounded-full shadow-lg hover:bg-teal-700 transition-all duration-300 transform hover:scale-110 z-20"
          :class="{ 'opacity-0 pointer-events-none': !showBackToTop, 'opacity-100': showBackToTop }"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M5 10l7-7m0 0l7 7m-7-7v18"
            />
          </svg>
        </button>

        <!-- Footer -->
        <footer class="text-center py-6 md:py-8 text-gray-600">
          <p>
            Dibuat oleh
            <a href="https://rfkinrikhwan.my.id" target="_blank" rel="noopener noreferrer"
              >Rifki Nur Ikhwan</a
            >
            and M Faiz Pratama Iwani
          </p>
          <p class="text-sm mt-2">© {{ new Date().getFullYear() }} Belajar Bareng Kami</p>
        </footer>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// State untuk section yang aktif - pastikan terisi nilai default
const activeSection = ref('lan')

// Data untuk navigasi
const sections = [
  { id: 'lan', name: 'LAN' },
  { id: 'wan', name: 'WAN' },
  { id: 'man', name: 'MAN' },
  { id: 'domain', name: 'Domain' },
  { id: 'hosting', name: 'Hosting' },
]

// Back to top functionality
const showBackToTop = ref(false)

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}

const checkScroll = () => {
  showBackToTop.value = window.scrollY > 300
}

onMounted(() => {
  // Scroll to top when page loads
  window.scrollTo({
    top: 0,
    behavior: 'auto',
  })

  window.addEventListener('scroll', checkScroll)

  // Animasi jaringan di header
  const networkAnimation = document.querySelector('.network-animation')
  if (networkAnimation) {
    // Membuat efek animasi jaringan
    for (let i = 0; i < 20; i++) {
      const node = document.createElement('div')
      node.className = 'network-node'
      node.style.width = '4px'
      node.style.height = '4px'
      node.style.backgroundColor = 'white'
      node.style.borderRadius = '50%'
      node.style.position = 'absolute'
      node.style.top = `${Math.random() * 100}%`
      node.style.left = `${Math.random() * 100}%`
      node.style.opacity = '0.6'

      const line = document.createElement('div')
      line.className = 'network-line'
      line.style.height = '1px'
      line.style.backgroundColor = 'white'
      line.style.position = 'absolute'
      line.style.top = `${Math.random() * 100}%`
      line.style.left = '0'
      line.style.right = '0'
      line.style.opacity = '0.3'
      line.style.transform = `rotate(${Math.random() * 180}deg)`

      networkAnimation.appendChild(node)
      networkAnimation.appendChild(line)
    }
  }
})

onUnmounted(() => {
  window.removeEventListener('scroll', checkScroll)
})
</script>

<style>
/* Animasi transisi untuk perubahan section */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* Media queries untuk responsivitas */
@media (max-width: 640px) {
  pre {
    font-size: 0.75rem;
  }

  .nav-container {
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
  }
}

/* Animasi */
@keyframes pulse {
  0% {
    transform: scale(1);
    opacity: 0.7;
  }
  50% {
    transform: scale(1.1);
    opacity: 1;
  }
  100% {
    transform: scale(1);
    opacity: 0.7;
  }
}

.pulse {
  animation: pulse 1s ease-in-out;
}

.animate-fade-in {
  animation: fadeIn 1.5s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.animate-slide-up {
  animation: slideUp 1s ease-out;
}

@keyframes slideUp {
  from {
    transform: translateY(20px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

/* Network Animation */
.network-node {
  animation: blink 3s infinite alternate;
}

.network-line {
  animation: fade 4s infinite alternate;
}

@keyframes blink {
  0% {
    opacity: 0.2;
  }
  100% {
    opacity: 0.8;
  }
}

@keyframes fade {
  0% {
    opacity: 0.1;
  }
  100% {
    opacity: 0.4;
  }
}

/* Topology Animations */
.topology-star:hover > div,
.topology-bus:hover > div,
.topology-ring:hover > div {
  animation: pulse 1s infinite alternate;
}

/* LAN, WAN, MAN Example Animations */
.lan-example:hover > div,
.wan-example:hover > div,
.man-example:hover > div {
  transition: all 0.3s ease;
}

.lan-example:hover > div:not(.absolute),
.wan-example:hover > div:not(.absolute),
.man-example:hover > div:not(.absolute) {
  transform: scale(1.05);
}
</style>
