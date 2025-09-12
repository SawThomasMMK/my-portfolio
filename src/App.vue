<template>
  <div class="font-sans bg-gray-50 text-gray-800 dark:bg-gray-900 dark:text-gray-100 min-h-screen">
    <NavBar />

    <main>
      <FadeIn>
        <section id="home" class="h-screen flex flex-col justify-center items-center text-center">
          <h1 class="text-5xl font-bold">Hi, I'm <span class="text-blue-500">Thomas</span></h1>
          <p class="mt-4 text-lg">Aspiring Frontend Developer | JavaScript • Tailwind • Vue</p>
          <div class="mt-6 flex gap-3">
            <a
              href="#projects"
              class="px-6 py-3 bg-blue-500 text-white rounded-xl shadow hover:bg-blue-600 transition"
            >
              View My Work
            </a>
            <a
              href="/resume.pdf"
              target="_blank"
              rel="noopener noreferrer"
              class="px-6 py-3 border border-blue-500 text-blue-500 rounded-xl hover:bg-blue-50 dark:hover:bg-gray-800 transition"
            >
              Resume
            </a>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="about" class="pt-16 max-w-3xl mx-auto text-center">
          <h2 class="text-3xl font-bold mb-6">About Me</h2>
          <p class="text-lg">
            I’m a software engineering student passionate about building modern, responsive web apps
            with Vue and Tailwind. This portfolio showcases my journey, skills, and projects.
          </p>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="experience" class="pt-16">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Experience</h2>
            <div class="space-y-6">
              <div class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow">
                <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-2">
                  <h3 class="font-semibold">Role / Company</h3>
                  <p class="text-sm text-gray-500">Month YYYY – Month YYYY</p>
                </div>
                <ul class="list-disc list-inside text-sm space-y-1">
                  <li>Brief responsibility or achievement.</li>
                  <li>Another impact-focused bullet point.</li>
                </ul>
              </div>
              <div class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow">
                <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-2">
                  <h3 class="font-semibold">Academic Presentation — Conference Name</h3>
                  <p class="text-sm text-gray-500">Month YYYY</p>
                </div>
                <p class="text-sm">Presented on [topic]. Linked abstract or slides if available.</p>
              </div>
            </div>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="skills" class="py-16">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Skills</h2>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow">
                <h3 class="font-semibold mb-6">Building Competence In</h3>
                <ul class="flex flex-wrap gap-2 text-sm">
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    HTML
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    CSS
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    JavaScript
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    Vue 3
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    Vite
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    TailwindCSS
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    Node.js
                  </li>
                  <li
                    class="px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200"
                  >
                    Express
                  </li>
                </ul>
              </div>
              <div class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow">
                <h3 class="font-semibold mb-3">Familiar With</h3>
                <ul class="flex flex-wrap gap-2 text-sm">
                  <li class="px-3 py-1 rounded-full bg-gray-100 dark:bg-gray-700">C#</li>
                  <li class="px-3 py-1 rounded-full bg-gray-100 dark:bg-gray-700">Java</li>
                  <li class="px-3 py-1 rounded-full bg-gray-100 dark:bg-gray-700">Dart</li>
                  <li class="px-3 py-1 rounded-full bg-gray-100 dark:bg-gray-700">Flutter</li>
                  <li class="px-3 py-1 rounded-full bg-gray-100 dark:bg-gray-700">Spring Boot</li>
                  <li class="px-3 py-1 rounded-full bg-gray-100 dark:bg-gray-700">Bootstrap</li>
                </ul>
              </div>
            </div>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="projects" class="py-16 bg-gray-100 dark:bg-gray-800">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div style="--stagger: 0">
                <ProjectCard
                  title="My Portfolio"
                  description="This very site! Built with Vue 3 + TailwindCSS."
                  tech="Vue, Tailwind"
                  link="https://github.com/yourusername/portfolio"
                  image="https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=1200&auto=format&fit=crop"
                  imageAlt="Screenshot of portfolio website"
                />
              </div>
            </div>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="education" class="pt-16">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Education</h2>
            <div class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow">
              <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-2">
                <h3 class="font-semibold">BSc in [Your Program] — [Your University]</h3>
                <p class="text-sm text-gray-500">Expected Graduation: YYYY</p>
              </div>
              <p class="text-sm mb-2">
                Relevant coursework: Algorithms, Web Development, Databases, OOP
              </p>
            </div>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="contact" class="pt-16 pb-10 max-w-3xl mx-auto text-center">
          <h2 class="text-3xl font-bold mb-6">Contact Me</h2>
          <p class="mb-4">Let’s connect! You can reach me via email or social links below.</p>
          <div class="space-x-4">
            <a href="mailto:youremail@example.com" class="text-blue-500 hover:underline">Email</a>
            <a href="https://github.com/yourusername" class="text-blue-500 hover:underline"
              >GitHub</a
            >
            <a href="https://linkedin.com/in/yourusername" class="text-blue-500 hover:underline"
              >LinkedIn</a
            >
          </div>
        </section>
      </FadeIn>
    </main>

    <footer class="py-6 text-center text-sm text-gray-500 dark:text-gray-400">
      © 2025 Your Name. Built with Vue & Tailwind.
    </footer>
  </div>
</template>

<script setup>
import NavBar from './components/AppNavbar.vue'
import ProjectCard from './components/ProjectCard.vue'
import FadeIn from './components/FadeIn.vue'
</script>
