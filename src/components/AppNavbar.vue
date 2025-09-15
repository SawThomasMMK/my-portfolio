<template>
  <nav
    class="fixed top-0 w-full bg-white/90 dark:bg-gray-900/90 backdrop-blur-md shadow-lg border-b border-gray-200/20 dark:border-gray-700/20 z-50 transition-all duration-300"
  >
    <div class="max-w-6xl mx-auto px-4 flex justify-between items-center h-16">
      <!-- Logo -->
      <a
        href="#home"
        class="text-xl font-bold text-blue-600 dark:text-blue-400 hover:text-blue-700 dark:hover:text-blue-300 transition-colors duration-200"
      >
        <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent"
          >Thomas</span
        >
      </a>

      <!-- Desktop Navigation -->
      <ul class="hidden md:flex space-x-1">
        <li>
          <a
            href="#home"
            data-nav="home"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            Home
          </a>
        </li>
        <li>
          <a
            href="#about"
            data-nav="about"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            About
          </a>
        </li>
        <li>
          <a
            href="#education"
            data-nav="education"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            Education
          </a>
        </li>
        <li>
          <a
            href="#skills"
            data-nav="skills"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            Skills
          </a>
        </li>
        <li>
          <a
            href="#projects"
            data-nav="projects"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            Projects
          </a>
        </li>
        <li>
          <a
            href="#experience"
            data-nav="experience"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            Experience
          </a>
        </li>
        <li>
          <a
            href="#contact"
            data-nav="contact"
            class="nav-link px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
          >
            Contact
          </a>
        </li>
      </ul>

      <!-- Mobile Menu Button -->
      <button
        @click="toggleMobileMenu"
        class="md:hidden p-2 rounded-lg text-gray-600 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors duration-200"
        aria-label="Toggle mobile menu"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path
            v-if="!isMobileMenuOpen"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          ></path>
          <path
            v-else
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          ></path>
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="isMobileMenuOpen"
      class="md:hidden bg-white dark:bg-gray-900 border-t border-gray-200 dark:border-gray-700 shadow-lg"
    >
      <div class="px-4 py-2 space-y-1">
        <a
          href="#home"
          data-nav="home"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          Home
        </a>
        <a
          href="#about"
          data-nav="about"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          About
        </a>
        <a
          href="#education"
          data-nav="education"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          Education
        </a>
        <a
          href="#skills"
          data-nav="skills"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          Skills
        </a>
        <a
          href="#projects"
          data-nav="projects"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          Projects
        </a>
        <a
          href="#experience"
          data-nav="experience"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          Experience
        </a>
        <a
          href="#contact"
          data-nav="contact"
          @click="closeMobileMenu"
          class="nav-link block px-4 py-3 rounded-lg text-sm font-medium transition-all duration-200 hover:bg-blue-50 dark:hover:bg-blue-900/20"
        >
          Contact
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue'

let observer
const isMobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

onMounted(() => {
  const links = Array.from(document.querySelectorAll('a[data-nav]'))
  const linkById = new Map(links.map((a) => [a.getAttribute('data-nav'), a]))

  function setActive(id) {
    links.forEach((a) => a.classList.remove('is-active'))
    const active = linkById.get(id)
    if (active) {
      active.classList.add('is-active')
      active.setAttribute('aria-current', 'page')
    }
  }

  observer = new IntersectionObserver(
    (entries) => {
      const visible = entries
        .filter((e) => e.isIntersecting)
        .sort((a, b) => b.intersectionRatio - a.intersectionRatio)
      if (visible[0]) {
        setActive(visible[0].target.id)
      }
    },
    { threshold: [0.2, 0.4, 0.6], rootMargin: '-20% 0px -40% 0px' },
  )
  ;['home', 'about', 'education', 'skills', 'projects', 'experience', 'contact'].forEach((id) => {
    const section = document.getElementById(id)
    if (section) observer.observe(section)
  })

  // Close mobile menu when clicking outside
  document.addEventListener('click', (e) => {
    if (isMobileMenuOpen.value && !e.target.closest('nav')) {
      closeMobileMenu()
    }
  })
})

onUnmounted(() => {
  if (observer) observer.disconnect()
})
</script>

<style scoped>
.is-active {
  color: rgb(37 99 235);
  font-weight: 600;
}
</style>
