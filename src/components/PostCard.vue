<template>
  <article
    class="bg-white dark:bg-gray-700 rounded-xl shadow-md p-5 transition hover:shadow-lg focus-within:shadow-lg"
  >
    <h3 class="text-lg font-semibold mb-1">
      <a :href="link" target="_blank" rel="noopener noreferrer" class="hover:underline">{{
        title
      }}</a>
    </h3>
    <p class="text-sm text-gray-500 dark:text-gray-300 mb-3">{{ date }}</p>
    <p class="text-sm mb-4">{{ excerpt }}</p>
    <a :href="link" target="_blank" rel="noopener noreferrer" class="text-blue-500 hover:underline"
      >Read more →</a
    >
  </article>
</template>

<script setup>
defineProps({
  title: String,
  date: String,
  excerpt: String,
  link: String,
})
</script>
