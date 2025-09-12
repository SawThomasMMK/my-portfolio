<template>
  <nav class="fixed top-0 w-full bg-white/80 dark:bg-gray-900/80 backdrop-blur shadow-sm z-50">
    <div class="max-w-6xl mx-auto px-4 flex justify-between items-center h-16">
      <a href="#home" class="text-xl font-bold text-blue-500">MyPortfolio</a>
      <ul class="hidden md:flex space-x-6">
        <li><a href="#home" data-nav="home" class="hover:text-blue-500">Home</a></li>
        <li><a href="#about" data-nav="about" class="hover:text-blue-500">About</a></li>
        <li>
          <a href="#experience" data-nav="experience" class="hover:text-blue-500">Experience</a>
        </li>
        <li><a href="#skills" data-nav="skills" class="hover:text-blue-500">Skills</a></li>
        <li><a href="#projects" data-nav="projects" class="hover:text-blue-500">Projects</a></li>
        <li><a href="#education" data-nav="education" class="hover:text-blue-500">Education</a></li>
        <li><a href="#contact" data-nav="contact" class="hover:text-blue-500">Contact</a></li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { onMounted, onUnmounted } from 'vue'

let observer

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
  ;['home', 'about', 'experience', 'skills', 'projects', 'education', 'contact'].forEach((id) => {
    const section = document.getElementById(id)
    if (section) observer.observe(section)
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
