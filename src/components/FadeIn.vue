<template>
  <div ref="el" :class="['fade-in', { 'is-visible': isVisible }]">
    <slot />
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isVisible = ref(false)
const el = ref(null)
let observer

// Track scroll direction to decide animation origin (top vs bottom)
const lastScrollY = ref(0)
const scrollDirection = ref('down')

function handleScroll() {
  const currentY = window.scrollY || window.pageYOffset
  scrollDirection.value = currentY > lastScrollY.value ? 'down' : 'up'
  lastScrollY.value = currentY
}

onMounted(() => {
  // Initialize direction and CSS var before observing
  handleScroll()
  if (el.value) {
    el.value.style.setProperty(
      '--fade-translate',
      scrollDirection.value === 'down'
        ? 'calc(var(--motion-distance, 24px) * -1)'
        : 'calc(var(--motion-distance, 24px) * 1)',
    )
  }

  observer = new IntersectionObserver(
    ([entry]) => {
      const intersecting = entry.isIntersecting
      if (!intersecting) {
        // Update the off-screen translate based on latest scroll direction
        if (el.value) {
          el.value.style.setProperty(
            '--fade-translate',
            scrollDirection.value === 'down'
              ? 'calc(var(--motion-distance, 24px) * -1)'
              : 'calc(var(--motion-distance, 24px) * 1)',
          )
        }
      }
      isVisible.value = intersecting
    },
    { threshold: 0.12, rootMargin: '0px 0px -8% 0px' },
  )

  if (el.value) observer.observe(el.value)
  window.addEventListener('scroll', handleScroll, { passive: true })
})

onUnmounted(() => {
  if (observer && el.value) observer.unobserve(el.value)
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.fade-in {
  opacity: 0;
  transform: translateY(var(--fade-translate, var(--motion-distance, 24px)));
  transition:
    opacity var(--motion-duration, 0.8s) var(--motion-easing, ease),
    transform var(--motion-duration, 0.8s) var(--motion-easing, ease);
  transition-delay: calc(var(--stagger, 0) * 90ms);
  will-change: opacity, transform;
}
.fade-in.is-visible {
  opacity: 1;
  transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
  .fade-in {
    transition: none;
  }
}
</style>
