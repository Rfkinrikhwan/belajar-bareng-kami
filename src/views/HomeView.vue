<template>
  <div>
    <h1>Hello World</h1>
    <h2>Hello World</h2>
    <h3>Hello World</h3>
    <h4>Hello World</h4>
    <h6>Hello World</h6>

    <p>
      <hr/>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sunt, voluptate!
      Ab quod delectus animi ea explicabo ipsum! Dolor dolorem quisquam nemo
      repellendus, ea nesciunt quae magnam! Maxime impedit laboriosam sint sequi
      praesentium ex cum placeat tempore nam reiciendis, quo rem aperiam eaque
      officia beatae suscipit magnam eum omnis recusandae!
      <hr/>
      <br />
      <hr/>
      Animi re enim molestias earum sit suscipit, quasi harum voluptatem ex
      deleniti explicabo accusamus quisquam voluptatibus praesentium magnam fuga
      dolores quas numquam omnis impedit? Eaque cupiditate vitae atque sint
      ullam consequatur voluptates unde quos. Reiciendis odio fuga, autem
      obcaecati natus eaque sed voluptas explicabo, fugiat, facilis dignissimos
      alias ullam nulla officiis.
      <hr/>
    </p>

    <hr/>

    <ul>
      <li>Mangga</li>
      <li>Pisang</li>
      <li>Buah Naga</li>
      <li>Kiwi</li>
    </ul>

    <ol type="A">
      <li>Mangga</li>
      <li>Pisang</li>
      <li>Buah Naga</li>
      <li>Kiwi</li>
    </ol>

    <hr/>
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
