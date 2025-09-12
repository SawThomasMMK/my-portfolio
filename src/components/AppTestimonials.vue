<template>
  <section>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <blockquote
        v-for="(t, i) in testimonials"
        :key="i"
        class="bg-white dark:bg-gray-700 rounded-xl shadow-md p-6"
      >
        <p class="mb-3">“{{ t.quote }}”</p>
        <footer class="text-sm text-gray-600 dark:text-gray-300">
          — {{ t.author }}, {{ t.role }}
        </footer>
      </blockquote>
    </div>
  </section>
</template>

<script setup>
defineProps({
  testimonials: {
    type: Array,
    default: () => [
      {
        quote: 'Shows strong ownership and attention to detail.',
        author: 'Professor A',
        role: 'CS Dept',
      },
      {
        quote: 'Communicates clearly and delivers on time.',
        author: 'Team Lead',
        role: 'Hackathon',
      },
      { quote: 'Quick learner with solid fundamentals.', author: 'Mentor', role: 'Open Source' },
    ],
  },
})
</script>
