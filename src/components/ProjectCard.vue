<template>
  <div
    class="bg-white dark:bg-gray-700 rounded-xl shadow-md p-6 flex flex-col transition-transform duration-200 will-change-transform hover:shadow-lg hover:-translate-y-0.5 focus-within:shadow-lg focus-within:-translate-y-0.5"
  >
    <img
      v-if="image"
      :src="image"
      :alt="imageAlt || title"
      loading="lazy"
      decoding="async"
      class="w-full h-48 object-cover rounded-lg mb-4"
    />
    <h3 class="text-xl font-bold mb-2">{{ title }}</h3>
    <p class="flex-grow mb-4">{{ description }}</p>
    <p class="text-sm text-gray-500 dark:text-gray-300 mb-4">Tech: {{ tech }}</p>
    <a
      :href="link"
      target="_blank"
      rel="noopener noreferrer"
      class="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-400 transition"
    >
      View Project
    </a>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  tech: String,
  link: String,
  image: String,
  imageAlt: String,
})
</script>
