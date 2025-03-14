<template>
  <div class="min-h-screen bg-gradient-to-br from-indigo-100 to-purple-100 p-2 sm:p-4 md:p-6">
    <div class="max-w-5xl mx-auto">
      <!-- Header dengan Animasi -->
      <header class="text-center py-6 md:py-10 relative overflow-hidden">
        <div class="absolute inset-0 flex items-center justify-center opacity-10">
          <div class="code-animation text-9xl font-mono text-indigo-800">&lt;/&gt;</div>
        </div>
        <h1
          class="text-3xl md:text-4xl font-bold text-indigo-800 mb-2 relative z-10 animate-fade-in"
        >
          Dokumentasi Praktikum HTML
        </h1>
        <p class="text-base md:text-lg text-gray-600 animate-slide-up">
          Kumpulan contoh elemen dasar HTML
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
                  d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                />
              </svg>
              Beranda
            </a>
          </li>
          <li>
            <a
              href="/network-docs"
              class="px-3 py-1.5 md:px-4 md:py-2 rounded-md text-sm md:text-base whitespace-nowrap transition-all duration-300 transform hover:scale-105 bg-purple-600 text-white shadow-md flex items-center"
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
                  d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"
                />
              </svg>
              Dokumentasi Network
            </a>
          </li>
        </ul>
      </nav>

      <!-- Navigasi -->
      <nav
        class="bg-white rounded-lg shadow-md p-3 mb-6 md:mb-8 sticky top-14 md:top-24 z-10 overflow-x-auto"
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
                  ? 'bg-indigo-600 text-white shadow-md'
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
        <!-- HTML Definition Section -->
        <div v-if="activeSection === 'html-definition'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Pengertian HTML</h2>
            <p class="text-sm md:text-base text-gray-600">Apa itu HTML dan mengapa penting?</p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- HTML Definition -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Definisi HTML</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base mb-4">
                      <strong>HTML</strong> (HyperText Markup Language) adalah
                      <span class="bg-yellow-100 px-1 py-0.5 font-semibold">bahasa markup</span>
                      standar yang digunakan untuk membuat dan menyusun halaman web. HTML terdiri
                      dari serangkaian elemen yang memberi tahu browser bagaimana menampilkan
                      konten.
                    </p>
                    <div class="bg-red-50 border-l-4 border-red-500 p-4 mb-4">
                      <p class="text-red-700 font-medium">Penting untuk diingat:</p>
                      <p class="text-red-600">
                        HTML <span class="font-bold underline">bukan</span> bahasa pemrograman,
                        melainkan bahasa markup yang digunakan untuk mendeskripsikan struktur
                        halaman web.
                      </p>
                    </div>
                    <p class="text-gray-800 text-sm md:text-base">
                      HTML menggunakan "markup" untuk menganotasi teks, gambar, dan konten lainnya
                      untuk ditampilkan di browser web. HTML markup mencakup "elemen" khusus seperti
                      &lt;head&gt;, &lt;title&gt;, &lt;body&gt;, &lt;header&gt;, &lt;footer&gt;,
                      &lt;article&gt;, &lt;section&gt;, &lt;p&gt;, &lt;div&gt;, &lt;span&gt;,
                      &lt;img&gt;, dan banyak lainnya.
                    </p>
                  </div>
                </div>
              </div>

              <!-- HTML Structure -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Struktur Dasar HTML
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <div class="bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto mb-4">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;!DOCTYPE html&gt;
  &lt;html&gt;
    &lt;head&gt;
      &lt;title&gt;Judul Halaman&lt;/title&gt;
      &lt;meta charset="UTF-8"&gt;
      &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;h1&gt;Ini adalah Heading&lt;/h1&gt;
      &lt;p&gt;Ini adalah paragraf.&lt;/p&gt;
    &lt;/body&gt;
  &lt;/html&gt;</code></pre>
                    </div>
                    <div class="flex flex-col md:flex-row gap-4">
                      <div class="flex-1">
                        <h4 class="font-semibold text-indigo-700 mb-2">Komponen Utama:</h4>
                        <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base space-y-2">
                          <li><strong>&lt;!DOCTYPE html&gt;</strong>: Deklarasi tipe dokumen</li>
                          <li><strong>&lt;html&gt;</strong>: Elemen root dari halaman HTML</li>
                          <li>
                            <strong>&lt;head&gt;</strong>: Berisi meta-informasi tentang dokumen
                          </li>
                          <li><strong>&lt;title&gt;</strong>: Menentukan judul halaman</li>
                          <li><strong>&lt;body&gt;</strong>: Berisi konten yang terlihat</li>
                        </ul>
                      </div>
                      <div class="flex-1 mt-4 md:mt-0">
                        <div
                          class="html-structure-demo border border-gray-300 rounded-md overflow-hidden"
                        >
                          <div class="bg-blue-100 p-2 text-center text-sm border-b border-gray-300">
                            &lt;html&gt;
                          </div>
                          <div
                            class="bg-green-100 p-2 mx-4 mt-2 text-center text-sm border border-gray-300"
                          >
                            &lt;head&gt;
                          </div>
                          <div
                            class="bg-yellow-100 p-6 mx-8 my-2 text-center text-sm border border-gray-300"
                          >
                            &lt;title&gt;, &lt;meta&gt;, etc.
                          </div>
                          <div
                            class="bg-red-100 p-2 mx-4 text-center text-sm border border-gray-300"
                          >
                            &lt;body&gt;
                          </div>
                          <div
                            class="bg-purple-100 p-6 mx-8 my-2 text-center text-sm border border-gray-300"
                          >
                            Konten yang terlihat
                          </div>
                          <div class="p-2"></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- HTML vs Programming Languages -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    HTML vs Bahasa Pemrograman
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <div class="comparison-table overflow-x-auto">
                      <table
                        class="min-w-full border-collapse border border-gray-300 text-sm md:text-base"
                      >
                        <thead>
                          <tr class="bg-indigo-100">
                            <th class="border border-gray-300 p-2 md:p-3 text-left">Aspek</th>
                            <th class="border border-gray-300 p-2 md:p-3 text-left">
                              HTML (Markup)
                            </th>
                            <th class="border border-gray-300 p-2 md:p-3 text-left">
                              Bahasa Pemrograman
                            </th>
                          </tr>
                        </thead>
                        <tbody>
                          <tr class="hover:bg-gray-50 transition-colors">
                            <td class="border border-gray-300 p-2 md:p-3 font-medium">Tujuan</td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              Mendeskripsikan dan menstrukturkan konten
                            </td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              Membuat logika, algoritma, dan fungsionalitas
                            </td>
                          </tr>
                          <tr class="hover:bg-gray-50 transition-colors">
                            <td class="border border-gray-300 p-2 md:p-3 font-medium">Eksekusi</td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              Ditampilkan (rendered) oleh browser
                            </td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              Dieksekusi oleh compiler atau interpreter
                            </td>
                          </tr>
                          <tr class="hover:bg-gray-50 transition-colors">
                            <td class="border border-gray-300 p-2 md:p-3 font-medium">Kemampuan</td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              Tidak dapat membuat keputusan atau melakukan perhitungan
                            </td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              Dapat membuat keputusan, loop, dan operasi kompleks
                            </td>
                          </tr>
                          <tr class="hover:bg-gray-50 transition-colors">
                            <td class="border border-gray-300 p-2 md:p-3 font-medium">Contoh</td>
                            <td class="border border-gray-300 p-2 md:p-3">HTML, XML, Markdown</td>
                            <td class="border border-gray-300 p-2 md:p-3">
                              JavaScript, Python, Java, C++
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </div>
                    <div class="mt-4 text-sm md:text-base text-gray-700 italic">
                      <p>
                        Untuk membuat halaman web yang dinamis dan interaktif, HTML biasanya
                        dikombinasikan dengan CSS (untuk styling) dan JavaScript (untuk
                        fungsionalitas dan interaksi).
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Heading Section -->
        <div v-if="activeSection === 'heading'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Heading</h2>
            <p class="text-sm md:text-base text-gray-600">Elemen h1-h6 untuk judul dan subjudul</p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- h1 -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">h1 - Judul Utama</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <h1 class="text-3xl md:text-4xl font-bold text-gray-800">
                      Ini adalah Heading 1
                    </h1>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;h1&gt;Ini adalah Heading 1&lt;/h1&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- h2 -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">h2 - Sub Judul</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <h2 class="text-2xl md:text-3xl font-bold text-gray-800">
                      Ini adalah Heading 2
                    </h2>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;h2&gt;Ini adalah Heading 2&lt;/h2&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- h3 and h4 -->
              <div class="flex flex-col sm:flex-row gap-4">
                <div
                  class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 flex-1"
                >
                  <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                    <h3 class="font-medium text-gray-700 text-sm md:text-base">h3</h3>
                  </div>
                  <div class="p-4 md:p-6">
                    <div class="mb-4">
                      <h3 class="text-xl md:text-2xl font-bold text-gray-800">Heading 3</h3>
                      <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                        <pre
                          class="text-gray-300 text-xs md:text-sm font-mono"
                        ><code>&lt;h3&gt;Heading 3&lt;/h3&gt;</code></pre>
                      </div>
                    </div>
                  </div>
                </div>

                <div
                  class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 flex-1"
                >
                  <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                    <h3 class="font-medium text-gray-700 text-sm md:text-base">h4</h3>
                  </div>
                  <div class="p-4 md:p-6">
                    <div class="mb-4">
                      <h4 class="text-lg md:text-xl font-bold text-gray-800">Heading 4</h4>
                      <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                        <pre
                          class="text-gray-300 text-xs md:text-sm font-mono"
                        ><code>&lt;h4&gt;Heading 4&lt;/h4&gt;</code></pre>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- h5 and h6 -->
              <div class="flex flex-col sm:flex-row gap-4">
                <div
                  class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 flex-1"
                >
                  <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                    <h3 class="font-medium text-gray-700 text-sm md:text-base">h5</h3>
                  </div>
                  <div class="p-4 md:p-6">
                    <div class="mb-4">
                      <h5 class="text-base md:text-lg font-bold text-gray-800">Heading 5</h5>
                      <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                        <pre
                          class="text-gray-300 text-xs md:text-sm font-mono"
                        ><code>&lt;h5&gt;Heading 5&lt;/h5&gt;</code></pre>
                      </div>
                    </div>
                  </div>
                </div>

                <div
                  class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300 flex-1"
                >
                  <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                    <h3 class="font-medium text-gray-700 text-sm md:text-base">h6</h3>
                  </div>
                  <div class="p-4 md:p-6">
                    <div class="mb-4">
                      <h6 class="text-sm md:text-base font-bold text-gray-800">Heading 6</h6>
                      <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                        <pre
                          class="text-gray-300 text-xs md:text-sm font-mono"
                        ><code>&lt;h6&gt;Heading 6&lt;/h6&gt;</code></pre>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Paragraf Section -->
        <div v-if="activeSection === 'paragraph'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Paragraf</h2>
            <p class="text-sm md:text-base text-gray-600">Elemen p untuk membuat paragraf teks</p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- Paragraf Dasar -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Paragraf Dasar</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base">
                      Ini adalah contoh paragraf. Paragraf adalah elemen dasar untuk menampilkan
                      teks dalam HTML. Paragraf biasanya digunakan untuk mengelompokkan
                      kalimat-kalimat yang memiliki topik yang sama.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;Ini adalah contoh paragraf. Paragraf adalah elemen dasar untuk menampilkan teks dalam HTML. Paragraf biasanya digunakan untuk mengelompokkan kalimat-kalimat yang memiliki topik yang sama.&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Paragraf dengan Alignment -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Paragraf dengan Alignment
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-left mb-4 text-sm md:text-base">
                      Ini adalah paragraf dengan rata kiri (default).
                    </p>
                    <p class="text-gray-800 text-center mb-4 text-sm md:text-base">
                      Ini adalah paragraf dengan rata tengah.
                    </p>
                    <p class="text-gray-800 text-right mb-4 text-sm md:text-base">
                      Ini adalah paragraf dengan rata kanan.
                    </p>
                    <p class="text-gray-800 text-justify text-sm md:text-base">
                      Ini adalah paragraf dengan rata kiri dan kanan (justify). Teks akan
                      menyesuaikan untuk mengisi seluruh lebar kontainer. Ini berguna untuk teks
                      yang panjang dan membutuhkan tampilan yang rapi di kedua sisi.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p style="text-align: left;"&gt;Ini adalah paragraf dengan rata kiri (default).&lt;/p&gt;
  &lt;p style="text-align: center;"&gt;Ini adalah paragraf dengan rata tengah.&lt;/p&gt;
  &lt;p style="text-align: right;"&gt;Ini adalah paragraf dengan rata kanan.&lt;/p&gt;
  &lt;p style="text-align: justify;"&gt;Ini adalah paragraf dengan rata kiri dan kanan (justify).&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Paragraf dengan Formatting -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Paragraf dengan Formatting
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base">
                      Paragraf dapat berisi <strong>teks tebal</strong>, <em>teks miring</em>,
                      <u>teks bergaris bawah</u>, dan <mark>teks yang disorot</mark>.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;Paragraf dapat berisi &lt;strong&gt;teks tebal&lt;/strong&gt;, &lt;em&gt;teks miring&lt;/em&gt;, 
  &lt;u&gt;teks bergaris bawah&lt;/u&gt;, dan &lt;mark&gt;teks yang disorot&lt;/mark&gt;.&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Line Break Section -->
        <div v-if="activeSection === 'br'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Line Break</h2>
            <p class="text-sm md:text-base text-gray-600">Elemen br untuk membuat jeda baris</p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- Line Break Dasar -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Line Break Dasar</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base">
                      Ini adalah baris pertama.<br />Ini adalah baris kedua.<br />Ini adalah baris
                      ketiga.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre class="text-gray-300 text-xs md:text-sm font-mono"><code>&lt;p&gt;
    Ini adalah baris pertama.&lt;br&gt;
    Ini adalah baris kedua.&lt;br&gt;
    Ini adalah baris ketiga.
  &lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Line Break dalam Puisi -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Line Break dalam Puisi
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-sm md:text-base">
                      Mawar itu merah,<br />
                      Violet itu biru,<br />
                      Gula itu manis,<br />
                      Dan begitu juga kamu.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre class="text-gray-300 text-xs md:text-sm font-mono"><code>&lt;p&gt;
    Mawar itu merah,&lt;br&gt;
    Violet itu biru,&lt;br&gt;
    Gula itu manis,&lt;br&gt;
    Dan begitu juga kamu.
  &lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Line Break vs Paragraf -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Line Break vs Paragraf
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-4 text-sm md:text-base">
                      Ini adalah paragraf pertama.
                    </p>
                    <p class="text-gray-800 mb-4 text-sm md:text-base">
                      Ini adalah paragraf kedua dengan jarak yang lebih besar.
                    </p>
                    <p class="text-gray-800 text-sm md:text-base">
                      Ini adalah baris pertama dalam paragraf ketiga.<br />
                      Ini adalah baris kedua dalam paragraf yang sama dengan jarak yang lebih kecil.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;Ini adalah paragraf pertama.&lt;/p&gt;
  
  &lt;p&gt;Ini adalah paragraf kedua dengan jarak yang lebih besar.&lt;/p&gt;
  
  &lt;p&gt;
    Ini adalah baris pertama dalam paragraf ketiga.&lt;br&gt;
    Ini adalah baris kedua dalam paragraf yang sama dengan jarak yang lebih kecil.
  &lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Horizontal Rule Section -->
        <div v-if="activeSection === 'hr'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Horizontal Rule</h2>
            <p class="text-sm md:text-base text-gray-600">
              Elemen hr untuk membuat garis horizontal
            </p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- HR Dasar -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Horizontal Rule Dasar
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-4 text-sm md:text-base">
                      Teks sebelum garis horizontal.
                    </p>
                    <hr class="my-4 border-gray-300" />
                    <p class="text-gray-800 text-sm md:text-base">Teks setelah garis horizontal.</p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;Teks sebelum garis horizontal.&lt;/p&gt;
  &lt;hr&gt;
  &lt;p&gt;Teks setelah garis horizontal.&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- HR dengan Styling -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Horizontal Rule dengan Styling
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-4 text-sm md:text-base">Garis tipis (default):</p>
                    <hr class="my-4 border-gray-300" />

                    <p class="text-gray-800 mb-4 text-sm md:text-base">Garis tebal:</p>
                    <hr class="my-4 border-gray-300 border-2" />

                    <p class="text-gray-800 mb-4 text-sm md:text-base">Garis berwarna:</p>
                    <hr class="my-4 border-indigo-500" />

                    <p class="text-gray-800 mb-4 text-sm md:text-base">
                      Garis dengan lebar terbatas:
                    </p>
                    <hr class="my-4 border-gray-300 w-1/2 mx-auto" />

                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;Garis tipis (default):&lt;/p&gt;
  &lt;hr&gt;
  
  &lt;p&gt;Garis tebal:&lt;/p&gt;
  &lt;hr style="height: 2px;"&gt;
  
  &lt;p&gt;Garis berwarna:&lt;/p&gt;
  &lt;hr style="border-color: #6366f1;"&gt;
  
  &lt;p&gt;Garis dengan lebar terbatas:&lt;/p&gt;
  &lt;hr style="width: 50%; margin: auto;"&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- HR untuk Pemisah Konten -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Horizontal Rule untuk Pemisah Konten
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <h3 class="text-lg md:text-xl font-bold text-gray-800 mb-2">
                      Bagian 1: Pengenalan
                    </h3>
                    <p class="text-gray-800 mb-4 text-sm md:text-base">
                      Ini adalah konten untuk bagian pengenalan. Horizontal rule dapat digunakan
                      untuk memisahkan bagian-bagian dalam sebuah halaman web.
                    </p>

                    <hr class="my-6 border-gray-300" />

                    <h3 class="text-lg md:text-xl font-bold text-gray-800 mb-2">
                      Bagian 2: Pembahasan
                    </h3>
                    <p class="text-gray-800 mb-4 text-sm md:text-base">
                      Ini adalah konten untuk bagian pembahasan. Dengan menggunakan horizontal rule,
                      pembaca dapat dengan mudah melihat pemisahan antar bagian.
                    </p>

                    <hr class="my-6 border-gray-300" />

                    <h3 class="text-lg md:text-xl font-bold text-gray-800 mb-2">
                      Bagian 3: Kesimpulan
                    </h3>
                    <p class="text-gray-800 text-sm md:text-base">
                      Ini adalah konten untuk bagian kesimpulan. Horizontal rule membantu
                      meningkatkan keterbacaan dokumen yang panjang.
                    </p>

                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;h3&gt;Bagian 1: Pengenalan&lt;/h3&gt;
  &lt;p&gt;Ini adalah konten untuk bagian pengenalan...&lt;/p&gt;
  
  &lt;hr&gt;
  
  &lt;h3&gt;Bagian 2: Pembahasan&lt;/h3&gt;
  &lt;p&gt;Ini adalah konten untuk bagian pembahasan...&lt;/p&gt;
  
  &lt;hr&gt;
  
  &lt;h3&gt;Bagian 3: Kesimpulan&lt;/h3&gt;
  &lt;p&gt;Ini adalah konten untuk bagian kesimpulan...&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Sub & Sup Section -->
        <div v-if="activeSection === 'subsup'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Sub & Sup</h2>
            <p class="text-sm md:text-base text-gray-600">
              Elemen sub dan sup untuk teks subscript dan superscript
            </p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- Subscript -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Subscript (sub)</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-base md:text-lg">
                      H<sub>2</sub>O adalah rumus kimia untuk air.
                    </p>
                    <p class="text-gray-800 text-base md:text-lg mt-4">
                      Rumus kimia untuk karbon dioksida adalah CO<sub>2</sub>.
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;H&lt;sub&gt;2&lt;/sub&gt;O adalah rumus kimia untuk air.&lt;/p&gt;
  
  &lt;p&gt;Rumus kimia untuk karbon dioksida adalah CO&lt;sub&gt;2&lt;/sub&gt;.&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Superscript -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Superscript (sup)</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-base md:text-lg">
                      E = mc<sup>2</sup> adalah rumus terkenal dari Einstein.
                    </p>
                    <p class="text-gray-800 text-base md:text-lg mt-4">
                      2<sup>3</sup> = 8 (2 pangkat 3 sama dengan 8).
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;E = mc&lt;sup&gt;2&lt;/sup&gt; adalah rumus terkenal dari Einstein.&lt;/p&gt;
  
  &lt;p&gt;2&lt;sup&gt;3&lt;/sup&gt; = 8 (2 pangkat 3 sama dengan 8).&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Kombinasi Sub dan Sup -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Kombinasi Sub dan Sup
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 text-base md:text-lg">
                      Dalam matematika, kita sering menggunakan kombinasi subscript dan superscript,
                      seperti: x<sub>i</sub><sup>2</sup> + y<sub>i</sub><sup>2</sup> = r<sup>2</sup>
                    </p>
                    <p class="text-gray-800 text-base md:text-lg mt-4">
                      Persamaan kuadrat: ax<sup>2</sup> + bx + c = 0, dimana a<sub>0</sub> ≠ 0
                    </p>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;p&gt;Dalam matematika, kita sering menggunakan kombinasi subscript dan superscript, seperti: x&lt;sub&gt;i&lt;/sub&gt;&lt;sup&gt;2&lt;/sup&gt; + y&lt;sub&gt;i&lt;/sub&gt;&lt;sup&gt;2&lt;/sup&gt; = r&lt;sup&gt;2&lt;/sup&gt;&lt;/p&gt;
  
  &lt;p&gt;Persamaan kuadrat: ax&lt;sup&gt;2&lt;/sup&gt; + bx + c = 0, dimana a&lt;sub&gt;0&lt;/sub&gt; ≠ 0&lt;/p&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Blockquote Section -->
        <div v-if="activeSection === 'blockquote'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">Blockquote</h2>
            <p class="text-sm md:text-base text-gray-600">
              Elemen blockquote untuk menampilkan kutipan
            </p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- Blockquote Dasar -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Blockquote Dasar</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <blockquote
                      class="pl-4 border-l-4 border-indigo-500 italic text-gray-700 text-sm md:text-base"
                    >
                      Hidup adalah tentang membuat pilihan yang tepat, bukan pilihan yang sempurna.
                    </blockquote>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;blockquote&gt;
    Hidup adalah tentang membuat pilihan yang tepat, bukan pilihan yang sempurna.
  &lt;/blockquote&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Blockquote dengan Sumber -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Blockquote dengan Sumber
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <blockquote
                      class="pl-4 border-l-4 border-indigo-500 italic text-gray-700 text-sm md:text-base"
                    >
                      <p>Jadilah perubahan yang ingin kamu lihat di dunia.</p>
                      <footer class="text-right mt-2 text-gray-500 text-xs md:text-sm">
                        — Mahatma Gandhi
                      </footer>
                    </blockquote>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;blockquote&gt;
    &lt;p&gt;Jadilah perubahan yang ingin kamu lihat di dunia.&lt;/p&gt;
    &lt;footer&gt;— Mahatma Gandhi&lt;/footer&gt;
  &lt;/blockquote&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Blockquote dengan Styling -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Blockquote dengan Styling
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <blockquote
                      class="p-4 bg-indigo-50 border-l-4 border-indigo-500 rounded-r-lg shadow-md"
                    >
                      <p class="text-indigo-800 font-medium mb-2 text-sm md:text-base">
                        "Pendidikan adalah senjata paling ampuh yang dapat kamu gunakan untuk
                        mengubah dunia."
                      </p>
                      <footer class="text-right text-indigo-600 text-xs md:text-sm">
                        — Nelson Mandela
                      </footer>
                    </blockquote>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;blockquote style="padding: 1rem; background-color: #eef2ff; border-left: 4px solid #6366f1; border-radius: 0 0.5rem 0.5rem 0; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);"&gt;
    &lt;p style="color: #3730a3; font-weight: 500; margin-bottom: 0.5rem;"&gt;
      "Pendidikan adalah senjata paling ampuh yang dapat kamu gunakan untuk mengubah dunia."
    &lt;/p&gt;
    &lt;footer style="text-align: right; color: #6366f1;"&gt;— Nelson Mandela&lt;/footer&gt;
  &lt;/blockquote&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Nested Blockquote -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Nested Blockquote</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <blockquote
                      class="pl-4 border-l-4 border-indigo-500 text-gray-700 text-sm md:text-base"
                    >
                      <p>Dalam bukunya, penulis menyatakan:</p>
                      <blockquote class="pl-4 border-l-4 border-purple-500 mt-2 italic">
                        <p>Kreativitas adalah kecerdasan yang bersenang-senang.</p>
                        <footer class="text-right mt-2 text-gray-500 text-xs md:text-sm">
                          — Albert Einstein
                        </footer>
                      </blockquote>
                      <p class="mt-2">
                        Ini menunjukkan pentingnya keseimbangan antara kecerdasan dan kesenangan
                        dalam proses kreatif.
                      </p>
                    </blockquote>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;blockquote&gt;
    &lt;p&gt;Dalam bukunya, penulis menyatakan:&lt;/p&gt;
    &lt;blockquote&gt;
      &lt;p&gt;Kreativitas adalah kecerdasan yang bersenang-senang.&lt;/p&gt;
      &lt;footer&gt;— Albert Einstein&lt;/footer&gt;
    &lt;/blockquote&gt;
    &lt;p&gt;Ini menunjukkan pentingnya keseimbangan antara kecerdasan dan kesenangan dalam proses kreatif.&lt;/p&gt;
  &lt;/blockquote&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- List Section -->
        <div v-if="activeSection === 'list'" class="p-4 md:p-6">
          <div class="mb-6">
            <h2 class="text-xl md:text-2xl font-bold text-indigo-700">List</h2>
            <p class="text-sm md:text-base text-gray-600">
              Elemen ul, ol, dan dl untuk membuat daftar
            </p>
            <div class="h-1 w-20 bg-indigo-500 mt-2 rounded"></div>
          </div>

          <div class="bg-gray-50 p-4 md:p-6 rounded-lg mb-6 md:mb-8">
            <div class="grid grid-cols-1 gap-4">
              <!-- Unordered List -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Unordered List (ul)
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-2 text-sm md:text-base">Daftar buah-buahan:</p>
                    <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base">
                      <li class="hover:text-indigo-600 transition-colors duration-300">Apel</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Jeruk</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Pisang</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Mangga</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Anggur</li>
                    </ul>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre class="text-gray-300 text-xs md:text-sm font-mono"><code>&lt;ul&gt;
    &lt;li&gt;Apel&lt;/li&gt;
    &lt;li&gt;Jeruk&lt;/li&gt;
    &lt;li&gt;Pisang&lt;/li&gt;
    &lt;li&gt;Mangga&lt;/li&gt;
    &lt;li&gt;Anggur&lt;/li&gt;
  &lt;/ul&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Ordered List -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">Ordered List (ol)</h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-2 text-sm md:text-base">
                      Langkah-langkah membuat kue:
                    </p>
                    <ol class="list-decimal pl-5 text-gray-800 text-sm md:text-base">
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Siapkan bahan-bahan
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Campurkan tepung, gula, dan telur
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Aduk hingga merata
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Tuang ke dalam loyang
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Panggang selama 30 menit
                      </li>
                    </ol>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre class="text-gray-300 text-xs md:text-sm font-mono"><code>&lt;ol&gt;
    &lt;li&gt;Siapkan bahan-bahan&lt;/li&gt;
    &lt;li&gt;Campurkan tepung, gula, dan telur&lt;/li&gt;
    &lt;li&gt;Aduk hingga merata&lt;/li&gt;
    &lt;li&gt;Tuang ke dalam loyang&lt;/li&gt;
    &lt;li&gt;Panggang selama 30 menit&lt;/li&gt;
  &lt;/ol&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Ordered List dengan Atribut -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Ordered List dengan Atribut
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-2 text-sm md:text-base">Mulai dari nomor 5:</p>
                    <ol start="5" class="list-decimal pl-5 text-gray-800 text-sm md:text-base">
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Item kelima
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Item keenam
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Item ketujuh
                      </li>
                    </ol>

                    <p class="text-gray-800 mt-4 mb-2 text-sm md:text-base">Menggunakan huruf:</p>
                    <ol type="A" class="pl-5 text-gray-800 text-sm md:text-base">
                      <li class="hover:text-indigo-600 transition-colors duration-300">Item A</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Item B</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Item C</li>
                    </ol>

                    <p class="text-gray-800 mt-4 mb-2 text-sm md:text-base">
                      Menggunakan angka romawi:
                    </p>
                    <ol type="I" class="pl-5 text-gray-800 text-sm md:text-base">
                      <li class="hover:text-indigo-600 transition-colors duration-300">Item I</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Item II</li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">Item III</li>
                    </ol>

                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;!-- Mulai dari nomor 5 --&gt;
  &lt;ol start="5"&gt;
    &lt;li&gt;Item kelima&lt;/li&gt;
    &lt;li&gt;Item keenam&lt;/li&gt;
    &lt;li&gt;Item ketujuh&lt;/li&gt;
  &lt;/ol&gt;
  
  &lt;!-- Menggunakan huruf --&gt;
  &lt;ol type="A"&gt;
    &lt;li&gt;Item A&lt;/li&gt;
    &lt;li&gt;Item B&lt;/li&gt;
    &lt;li&gt;Item C&lt;/li&gt;
  &lt;/ol&gt;
  
  &lt;!-- Menggunakan angka romawi --&gt;
  &lt;ol type="I"&gt;
    &lt;li&gt;Item I&lt;/li&gt;
    &lt;li&gt;Item II&lt;/li&gt;
    &lt;li&gt;Item III&lt;/li&gt;
  &lt;/ol&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Nested List -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Nested List (Daftar Bersarang)
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-2 text-sm md:text-base">Menu makanan:</p>
                    <ul class="list-disc pl-5 text-gray-800 text-sm md:text-base">
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Makanan Pembuka
                        <ul class="list-circle pl-5 mt-1 mb-2">
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Salad
                          </li>
                          <li class="hover:text-indigo-600 transition-colors duration-300">Sup</li>
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Bruschetta
                          </li>
                        </ul>
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Makanan Utama
                        <ul class="list-circle pl-5 mt-1 mb-2">
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Nasi Goreng
                          </li>
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Steak
                            <ul class="list-square pl-5 mt-1 mb-2">
                              <li class="hover:text-indigo-600 transition-colors duration-300">
                                Rare
                              </li>
                              <li class="hover:text-indigo-600 transition-colors duration-300">
                                Medium
                              </li>
                              <li class="hover:text-indigo-600 transition-colors duration-300">
                                Well Done
                              </li>
                            </ul>
                          </li>
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Pasta
                          </li>
                        </ul>
                      </li>
                      <li class="hover:text-indigo-600 transition-colors duration-300">
                        Makanan Penutup
                        <ul class="list-circle pl-5 mt-1">
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Es Krim
                          </li>
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Puding
                          </li>
                          <li class="hover:text-indigo-600 transition-colors duration-300">
                            Buah-buahan
                          </li>
                        </ul>
                      </li>
                    </ul>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre class="text-gray-300 text-xs md:text-sm font-mono"><code>&lt;ul&gt;
    &lt;li&gt;Makanan Pembuka
      &lt;ul&gt;
        &lt;li&gt;Salad&lt;/li&gt;
        &lt;li&gt;Sup&lt;/li&gt;
        &lt;li&gt;Bruschetta&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
    &lt;li&gt;Makanan Utama
      &lt;ul&gt;
        &lt;li&gt;Nasi Goreng&lt;/li&gt;
        &lt;li&gt;Steak
          &lt;ul&gt;
            &lt;li&gt;Rare&lt;/li&gt;
            &lt;li&gt;Medium&lt;/li&gt;
            &lt;li&gt;Well Done&lt;/li&gt;
          &lt;/ul&gt;
        &lt;/li&gt;
        &lt;li&gt;Pasta&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
    &lt;li&gt;Makanan Penutup
      &lt;ul&gt;
        &lt;li&gt;Es Krim&lt;/li&gt;
        &lt;li&gt;Puding&lt;/li&gt;
        &lt;li&gt;Buah-buahan&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
  &lt;/ul&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Definition List -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    Definition List (dl)
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-2 text-sm md:text-base">Istilah dalam HTML:</p>
                    <dl class="text-gray-800 text-sm md:text-base">
                      <dt class="font-bold mt-2 text-indigo-700">HTML</dt>
                      <dd
                        class="ml-4 hover:bg-indigo-50 transition-colors duration-300 p-1 rounded"
                      >
                        HyperText Markup Language, bahasa markup standar untuk membuat halaman web.
                      </dd>

                      <dt class="font-bold mt-3 text-indigo-700">CSS</dt>
                      <dd
                        class="ml-4 hover:bg-indigo-50 transition-colors duration-300 p-1 rounded"
                      >
                        Cascading Style Sheets, bahasa yang digunakan untuk menggambarkan tampilan
                        dan format dokumen HTML.
                      </dd>

                      <dt class="font-bold mt-3 text-indigo-700">JavaScript</dt>
                      <dd
                        class="ml-4 hover:bg-indigo-50 transition-colors duration-300 p-1 rounded"
                      >
                        Bahasa pemrograman yang memungkinkan implementasi fitur kompleks pada
                        halaman web.
                      </dd>
                    </dl>
                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre class="text-gray-300 text-xs md:text-sm font-mono"><code>&lt;dl&gt;
    &lt;dt&gt;HTML&lt;/dt&gt;
    &lt;dd&gt;HyperText Markup Language, bahasa markup standar untuk membuat halaman web.&lt;/dd&gt;
    
    &lt;dt&gt;CSS&lt;/dt&gt;
    &lt;dd&gt;Cascading Style Sheets, bahasa yang digunakan untuk menggambarkan tampilan dan format dokumen HTML.&lt;/dd&gt;
    
    &lt;dt&gt;JavaScript&lt;/dt&gt;
    &lt;dd&gt;Bahasa pemrograman yang memungkinkan implementasi fitur kompleks pada halaman web.&lt;/dd&gt;
  &lt;/dl&gt;</code></pre>
                    </div>
                  </div>
                </div>
              </div>

              <!-- List dengan Styling -->
              <div
                class="border border-gray-200 rounded-lg overflow-hidden bg-white shadow-sm hover:shadow-md transition-shadow transform hover:-translate-y-1 duration-300"
              >
                <div class="p-3 md:p-4 border-b border-gray-100 bg-gray-50">
                  <h3 class="font-medium text-gray-700 text-sm md:text-base">
                    List dengan Styling
                  </h3>
                </div>
                <div class="p-4 md:p-6">
                  <div class="mb-4">
                    <p class="text-gray-800 mb-2 text-sm md:text-base">List dengan ikon kustom:</p>
                    <ul class="space-y-2 text-sm md:text-base">
                      <li
                        class="flex items-start transform hover:translate-x-2 transition-transform duration-300"
                      >
                        <span
                          class="inline-flex items-center justify-center w-6 h-6 mr-2 bg-green-500 rounded-full text-white flex-shrink-0"
                          >✓</span
                        >
                        <span>Fitur yang sudah selesai</span>
                      </li>
                      <li
                        class="flex items-start transform hover:translate-x-2 transition-transform duration-300"
                      >
                        <span
                          class="inline-flex items-center justify-center w-6 h-6 mr-2 bg-yellow-500 rounded-full text-white flex-shrink-0"
                          >!</span
                        >
                        <span>Fitur yang sedang dikerjakan</span>
                      </li>
                      <li
                        class="flex items-start transform hover:translate-x-2 transition-transform duration-300"
                      >
                        <span
                          class="inline-flex items-center justify-center w-6 h-6 mr-2 bg-red-500 rounded-full text-white flex-shrink-0"
                          >✗</span
                        >
                        <span>Fitur yang belum dimulai</span>
                      </li>
                    </ul>

                    <p class="text-gray-800 mt-6 mb-2 text-sm md:text-base">List horizontal:</p>
                    <ul class="flex flex-wrap gap-4 text-sm md:text-base">
                      <li
                        class="bg-indigo-100 px-3 py-1 rounded-full text-indigo-800 hover:bg-indigo-200 transition-colors duration-300 transform hover:scale-110"
                      >
                        HTML
                      </li>
                      <li
                        class="bg-indigo-100 px-3 py-1 rounded-full text-indigo-800 hover:bg-indigo-200 transition-colors duration-300 transform hover:scale-110"
                      >
                        CSS
                      </li>
                      <li
                        class="bg-indigo-100 px-3 py-1 rounded-full text-indigo-800 hover:bg-indigo-200 transition-colors duration-300 transform hover:scale-110"
                      >
                        JavaScript
                      </li>
                      <li
                        class="bg-indigo-100 px-3 py-1 rounded-full text-indigo-800 hover:bg-indigo-200 transition-colors duration-300 transform hover:scale-110"
                      >
                        Vue.js
                      </li>
                    </ul>

                    <div class="mt-4 bg-gray-800 p-3 md:p-4 rounded-md overflow-x-auto">
                      <pre
                        class="text-gray-300 text-xs md:text-sm font-mono"
                      ><code>&lt;!-- List dengan ikon kustom --&gt;
  &lt;ul&gt;
    &lt;li&gt;
      &lt;span style="display: inline-flex; align-items: center; justify-content: center; width: 1.5rem; height: 1.5rem; margin-right: 0.5rem; background-color: #10b981; border-radius: 9999px; color: white;"&gt;✓&lt;/span&gt;
      &lt;span&gt;Fitur yang sudah selesai&lt;/span&gt;
    &lt;/li&gt;
    &lt;li&gt;
      &lt;span style="display: inline-flex; align-items: center; justify-content: center; width: 1.5rem; height: 1.5rem; margin-right: 0.5rem; background-color: #f59e0b; border-radius: 9999px; color: white;"&gt;!&lt;/span&gt;
      &lt;span&gt;Fitur yang sedang dikerjakan&lt;/span&gt;
    &lt;/li&gt;
    &lt;li&gt;
      &lt;span style="display: inline-flex; align-items: center; justify-content: center; width: 1.5rem; height: 1.5rem; margin-right: 0.5rem; background-color: #ef4444; border-radius: 9999px; color: white;"&gt;✗&lt;/span&gt;
      &lt;span&gt;Fitur yang belum dimulai&lt;/span&gt;
    &lt;/li&gt;
  &lt;/ul&gt;
  
  &lt;!-- List horizontal --&gt;
  &lt;ul style="display: flex; flex-wrap: wrap; gap: 1rem;"&gt;
    &lt;li style="background-color: #e0e7ff; padding: 0.25rem 0.75rem; border-radius: 9999px; color: #4f46e5;"&gt;HTML&lt;/li&gt;
    &lt;li style="background-color: #e0e7ff; padding: 0.25rem 0.75rem; border-radius: 9999px; color: #4f46e5;"&gt;CSS&lt;/li&gt;
    &lt;li style="background-color: #e0e7ff; padding: 0.25rem 0.75rem; border-radius: 9999px; color: #4f46e5;"&gt;JavaScript&lt;/li&gt;
    &lt;li style="background-color: #e0e7ff; padding: 0.25rem 0.75rem; border-radius: 9999px; color: #4f46e5;"&gt;Vue.js&lt;/li&gt;
  &lt;/ul&gt;</code></pre>
                    </div>
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
        class="fixed bottom-6 right-6 bg-indigo-600 text-white p-3 rounded-full shadow-lg hover:bg-indigo-700 transition-all duration-300 transform hover:scale-110 z-20"
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
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// State untuk section yang aktif - pastikan terisi nilai default
const activeSection = ref('html-definition')

// Data untuk navigasi
const sections = [
  { id: 'html-definition', name: 'Pengertian HTML' },
  { id: 'heading', name: 'Heading' },
  { id: 'paragraph', name: 'Paragraf' },
  { id: 'br', name: 'Line Break' },
  { id: 'hr', name: 'Horizontal Rule' },
  { id: 'subsup', name: 'Sub & Sup' },
  { id: 'blockquote', name: 'Blockquote' },
  { id: 'list', name: 'List' },
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

  // Animasi kode di header
  const codeAnimation = document.querySelector('.code-animation')
  if (codeAnimation) {
    setInterval(() => {
      codeAnimation.classList.add('pulse')
      setTimeout(() => {
        codeAnimation.classList.remove('pulse')
      }, 1000)
    }, 3000)
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

/* Styling untuk list */
.list-circle {
  list-style-type: circle;
}
.list-square {
  list-style-type: square;
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

/* HTML Structure Demo Animation */
.html-structure-demo {
  transition: all 0.3s ease;
}

.html-structure-demo:hover {
  transform: scale(1.02);
  box-shadow:
    0 10px 15px -3px rgba(0, 0, 0, 0.1),
    0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.html-structure-demo > div {
  transition: all 0.3s ease;
}

.html-structure-demo:hover > div {
  border-color: #6366f1;
}

/* Code Animation */
.code-animation {
  animation: float 6s ease-in-out infinite;
  opacity: 0.7;
}

@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}
</style>
