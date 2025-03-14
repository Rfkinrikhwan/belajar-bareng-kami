<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 to-slate-100">
    <!-- Hero Section with Animated Background -->
    <div class="relative overflow-hidden bg-gradient-to-r from-blue-600 to-purple-600 text-white">
      <!-- Animated Background Elements -->
      <div class="absolute inset-0 overflow-hidden">
        <div class="particles-container"></div>
      </div>

      <div class="container mx-auto px-4 py-16 md:py-24 relative z-10">
        <div class="max-w-4xl mx-auto text-center">
          <h1 class="text-4xl md:text-6xl font-bold mb-4 animate-fade-in">Belajar Bareng Kami</h1>
          <p class="text-xl md:text-2xl mb-8 text-blue-100 animate-slide-up">
            Pelajari HTML, Jaringan, dan Konsep Domain dengan cara yang menarik
          </p>
          <div class="flex flex-wrap justify-center gap-4 animate-bounce-in">
            <button
              @click="scrollToSection('documentation')"
              class="px-6 py-3 bg-white text-blue-600 rounded-full font-semibold hover:bg-blue-50 transition-all duration-300 transform hover:scale-105 shadow-lg"
            >
              Jelajahi Dokumentasi
            </button>
            <button
              @click="scrollToSection('about')"
              class="px-6 py-3 bg-transparent border-2 border-white text-white rounded-full font-semibold hover:bg-white/10 transition-all duration-300 transform hover:scale-105"
            >
              Tentang Kami
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Documentation Cards Section -->
    <div id="documentation" class="container mx-auto px-4 py-16 md:py-24">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Pilih Dokumentasi</h2>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto">
          Kami menyediakan dokumentasi interaktif untuk membantu Anda memahami konsep dasar HTML dan
          Jaringan Komputer
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
        <!-- HTML Documentation Card -->
        <div
          class="doc-card bg-white rounded-xl shadow-xl overflow-hidden transform transition-all duration-500 hover:shadow-2xl hover:-translate-y-2"
        >
          <div class="h-48 bg-gradient-to-r from-indigo-500 to-purple-600 relative overflow-hidden">
            <!-- HTML Code Animation -->
            <div class="absolute inset-0 flex items-center justify-center opacity-20">
              <div class="html-animation text-9xl font-mono text-white">&lt;/&gt;</div>
            </div>
            <div class="absolute inset-0 flex items-center justify-center">
              <h3 class="text-3xl font-bold text-white">HTML Documentation</h3>
            </div>
          </div>
          <div class="p-6">
            <p class="text-gray-600 mb-6">
              Pelajari elemen-elemen dasar HTML seperti heading, paragraf, list, dan banyak lagi.
              Dokumentasi ini menyediakan contoh kode dan penjelasan yang mudah dipahami.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm"
                >Heading</span
              >
              <span class="px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm"
                >Paragraf</span
              >
              <span class="px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">List</span>
              <span class="px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm"
                >Blockquote</span
              >
              <span class="px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm"
                >Dan lainnya</span
              >
            </div>
            <button
              @click="navigateToHtml"
              class="w-full py-3 bg-indigo-600 cursor-pointer text-white rounded-lg font-semibold hover:bg-indigo-700 transition-colors duration-300 flex items-center justify-center gap-2"
            >
              Buka Dokumentasi HTML
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M10.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L12.586 11H5a1 1 0 110-2h7.586l-2.293-2.293a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                />
              </svg>
            </button>
          </div>
        </div>

        <!-- Network Documentation Card -->
        <div
          class="doc-card bg-white rounded-xl shadow-xl overflow-hidden transform transition-all duration-500 hover:shadow-2xl hover:-translate-y-2"
        >
          <div class="h-48 bg-gradient-to-r from-teal-500 to-green-600 relative overflow-hidden">
            <!-- Network Animation -->
            <div class="absolute inset-0 flex items-center justify-center">
              <div class="network-icon-container relative w-32 h-32">
                <div class="absolute inset-0 bg-white/20 rounded-full"></div>
                <div
                  class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-4 h-4 bg-white rounded-full"
                ></div>
                <div
                  class="absolute top-0 left-1/2 transform -translate-x-1/2 w-3 h-3 bg-white rounded-full"
                ></div>
                <div class="absolute top-1/4 right-0 w-3 h-3 bg-white rounded-full"></div>
                <div class="absolute bottom-1/4 right-0 w-3 h-3 bg-white rounded-full"></div>
                <div
                  class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-3 h-3 bg-white rounded-full"
                ></div>
                <div class="absolute bottom-1/4 left-0 w-3 h-3 bg-white rounded-full"></div>
                <div class="absolute top-1/4 left-0 w-3 h-3 bg-white rounded-full"></div>
                <!-- Lines -->
                <div
                  class="absolute top-0 left-1/2 transform -translate-x-1/2 w-px h-16 bg-white/60"
                ></div>
                <div class="absolute top-1/4 right-0 w-16 h-px bg-white/60"></div>
                <div class="absolute bottom-1/4 right-0 w-16 h-px bg-white/60"></div>
                <div
                  class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-px h-16 bg-white/60"
                ></div>
                <div class="absolute bottom-1/4 left-0 w-16 h-px bg-white/60"></div>
                <div class="absolute top-1/4 left-0 w-16 h-px bg-white/60"></div>
              </div>
            </div>
            <div class="absolute inset-0 flex items-center justify-center">
              <h3 class="text-3xl font-bold text-white">Network & Domain</h3>
            </div>
          </div>
          <div class="p-6">
            <p class="text-gray-600 mb-6">
              Pelajari konsep jaringan komputer seperti LAN, WAN, MAN, serta pengertian domain dan
              hosting. Dokumentasi ini dilengkapi dengan ilustrasi dan contoh implementasi.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="px-3 py-1 bg-teal-100 text-teal-800 rounded-full text-sm">LAN</span>
              <span class="px-3 py-1 bg-teal-100 text-teal-800 rounded-full text-sm">WAN</span>
              <span class="px-3 py-1 bg-teal-100 text-teal-800 rounded-full text-sm">MAN</span>
              <span class="px-3 py-1 bg-teal-100 text-teal-800 rounded-full text-sm">Domain</span>
              <span class="px-3 py-1 bg-teal-100 text-teal-800 rounded-full text-sm">Hosting</span>
            </div>
            <button
              @click="navigateToNetwork"
              class="w-full py-3 bg-teal-600 cursor-pointer text-white rounded-lg font-semibold hover:bg-teal-700 transition-colors duration-300 flex items-center justify-center gap-2"
            >
              Buka Dokumentasi Network
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M10.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L12.586 11H5a1 1 0 110-2h7.586l-2.293-2.293a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Features Section -->
    <div class="bg-gray-50 py-16 md:py-24">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Fitur Dokumentasi</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">
            Dokumentasi kami dirancang untuk memberikan pengalaman belajar yang optimal
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
          <!-- Feature 1 -->
          <div
            class="feature-card bg-white p-6 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300"
          >
            <div
              class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-4 mx-auto"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-8 w-8 text-blue-600"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"
                />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-center mb-2">Interaktif</h3>
            <p class="text-gray-600 text-center">
              Dokumentasi dilengkapi dengan elemen interaktif untuk memudahkan pemahaman konsep
            </p>
          </div>

          <!-- Feature 2 -->
          <div
            class="feature-card bg-white p-6 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300"
          >
            <div
              class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-4 mx-auto"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-8 w-8 text-purple-600"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"
                />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-center mb-2">Responsif</h3>
            <p class="text-gray-600 text-center">
              Tampilan yang responsif dan optimal di berbagai perangkat, dari desktop hingga mobile
            </p>
          </div>

          <!-- Feature 3 -->
          <div
            class="feature-card bg-white p-6 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300"
          >
            <div
              class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mb-4 mx-auto"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-8 w-8 text-green-600"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
                />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-center mb-2">Komprehensif</h3>
            <p class="text-gray-600 text-center">
              Materi lengkap dengan contoh kode, ilustrasi, dan penjelasan yang mudah dipahami
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- About Section -->
    <div id="about" class="container mx-auto px-4 py-16 md:py-24">
      <div class="max-w-4xl mx-auto">
        <div class="text-center mb-12">
          <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Tentang Kami</h2>
          <p class="text-lg text-gray-600">
            Kami berkomitmen untuk menyediakan materi pembelajaran yang berkualitas dan mudah
            diakses
          </p>
        </div>

        <div class="bg-white p-8 rounded-xl shadow-lg">
          <div class="prose prose-lg max-w-none">
            <p>
              Dokumentasi ini dibuat sebagai bagian dari proyek pembelajaran untuk membantu
              mahasiswa dan siapa saja yang ingin mempelajari dasar-dasar HTML dan konsep jaringan
              komputer. Kami percaya bahwa pembelajaran akan lebih efektif jika disajikan dengan
              cara yang menarik dan interaktif.
            </p>
            <p>Materi yang disajikan mencakup:</p>
            <ul>
              <li>Dasar-dasar HTML dan elemen-elemennya</li>
              <li>Konsep jaringan komputer (LAN, WAN, MAN)</li>
              <li>Pengertian domain dan hosting</li>
              <li>Contoh implementasi dan ilustrasi visual</li>
            </ul>
            <p>
              Dokumentasi ini akan terus diperbarui dan ditingkatkan untuk memberikan pengalaman
              belajar yang lebih baik. Jika Anda memiliki saran atau masukan, jangan ragu untuk
              menghubungi kami.
            </p>
            <div class="mt-8 text-center">
              <p class="font-semibold">Dibuat oleh:</p>
              <p class="text-xl font-bold">
                <a
                  href="https://rfkinrikhwan.my.id"
                  class="text-blue-600"
                  target="_blank"
                  rel="noopener noreferrer"
                  >Rifki Nur Ikhwan</a
                >
                and M Faiz Pratama Iwani
              </p>
              <p class="text-sm text-gray-500 mt-2">
                © {{ new Date().getFullYear() }} Belajar Bareng Kami
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Floating Action Button -->
    <div class="fixed bottom-6 right-6 z-50 flex flex-col items-end space-y-2">
      <div
        v-if="showFabMenu"
        class="fab-menu bg-white rounded-lg shadow-xl p-2 mb-2 transform transition-all duration-300"
        :class="showFabMenu ? 'scale-100 opacity-100' : 'scale-95 opacity-0'"
      >
        <div class="flex flex-col space-y-2">
          <button
            @click="navigateToHtml"
            class="flex items-center justify-start px-4 py-2 bg-indigo-100 text-indigo-700 rounded-lg hover:bg-indigo-200 transition-colors duration-300 w-64"
          >
            <span class="mr-2">&lt;/&gt;</span>
            <span>HTML Docs</span>
          </button>
          <button
            @click="navigateToNetwork"
            class="flex items-center justify-start px-4 py-2 bg-teal-100 text-teal-700 rounded-lg hover:bg-teal-200 transition-colors duration-300 w-64"
          >
            <span class="mr-2">🌐</span>
            <span>Network Docs</span>
          </button>
          <button
            @click="scrollToTop"
            class="flex items-center justify-start px-4 py-2 bg-gray-100 text-gray-700 rounded-lg hover:bg-gray-200 transition-colors duration-300 w-64"
          >
            <span class="mr-2">⬆️</span>
            <span>Kembali ke Atas</span>
          </button>
        </div>
      </div>

      <button
        @click="toggleFabMenu"
        class="w-14 h-14 bg-blue-600 text-white rounded-full shadow-lg hover:bg-blue-700 transition-colors duration-300 flex items-center justify-center focus:outline-none"
      >
        <svg
          v-if="!showFabMenu"
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
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
        <svg
          v-else
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
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

import { useRouter } from 'vue-router'

const router = useRouter()

// State for FAB menu
const showFabMenu = ref(false)
const showBackToTop = ref(false)

// Toggle FAB menu
const toggleFabMenu = () => {
  showFabMenu.value = !showFabMenu.value
}

// Scroll to section
const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}

// Scroll to top
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}

// Check scroll position
const checkScroll = () => {
  showBackToTop.value = window.scrollY > 300

  // Close FAB menu when scrolling
  if (showFabMenu.value && window.scrollY > 100) {
    showFabMenu.value = false
  }
}

// Navigation functions
const navigateToHtml = () => {
  // Replace with actual navigation logic or URL
  router.push({ name: 'html-docs' })
  // window.location.href = '/html-documentation'
}

const navigateToNetwork = () => {
  // Replace with actual navigation logic or URL
  router.push({ name: 'network-docs' })
  // window.location.href = '/network-documentation'
}

onMounted(() => {
  window.addEventListener('scroll', checkScroll)

  // Create particles for the hero section
  const particlesContainer = document.querySelector('.particles-container')
  if (particlesContainer) {
    for (let i = 0; i < 50; i++) {
      const particle = document.createElement('div')
      particle.className = 'particle'
      particle.style.width = `${Math.random() * 5 + 1}px`
      particle.style.height = particle.style.width
      particle.style.backgroundColor = 'rgba(255, 255, 255, 0.5)'
      particle.style.borderRadius = '50%'
      particle.style.position = 'absolute'
      particle.style.top = `${Math.random() * 100}%`
      particle.style.left = `${Math.random() * 100}%`
      particle.style.animation = `float ${Math.random() * 10 + 5}s linear infinite`
      particlesContainer.appendChild(particle)
    }
  }

  // Animate HTML code in the HTML card
  const htmlAnimation = document.querySelector('.html-animation')
  if (htmlAnimation) {
    setInterval(() => {
      htmlAnimation.classList.add('pulse')
      setTimeout(() => {
        htmlAnimation.classList.remove('pulse')
      }, 1000)
    }, 3000)
  }

  // Animate network nodes in the Network card
  const networkNodes = document.querySelectorAll('.network-icon-container div')
  if (networkNodes.length > 0) {
    networkNodes.forEach((node, index) => {
      if (index > 0) {
        // Skip the first div which is the background
        node.style.animation = `pulse ${Math.random() * 2 + 1}s infinite alternate ${Math.random() * 2}s`
      }
    })
  }
})

onUnmounted(() => {
  window.removeEventListener('scroll', checkScroll)
})
</script>

<style>
/* Animations */
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

.animate-bounce-in {
  animation: bounceIn 1s ease-out;
}

@keyframes bounceIn {
  0% {
    transform: scale(0.8);
    opacity: 0;
  }
  50% {
    transform: scale(1.05);
    opacity: 1;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}

/* Floating particles animation */
@keyframes float {
  0% {
    transform: translateY(0) translateX(0);
    opacity: 0;
  }
  50% {
    opacity: 0.8;
  }
  100% {
    transform: translateY(-100px) translateX(100px);
    opacity: 0;
  }
}

/* Feature cards hover effect */
.feature-card:hover {
  transform: translateY(-5px);
  transition: transform 0.3s ease;
}

/* Doc cards hover effect */
.doc-card:hover .html-animation,
.doc-card:hover .network-icon-container {
  transform: scale(1.1);
  transition: transform 0.5s ease;
}

/* Network icon animation */
.network-icon-container div {
  transition: all 0.3s ease;
}

.network-icon-container:hover div {
  opacity: 1;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .feature-card {
    padding: 1rem;
  }

  .doc-card .h-48 {
    height: 10rem;
  }
}

/* Prose styling for about section */
.prose ul {
  list-style-type: disc;
  padding-left: 1.5rem;
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}

.prose p {
  margin-top: 1rem;
  margin-bottom: 1rem;
}
</style>
