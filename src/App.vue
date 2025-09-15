<template>
  <div class="font-sans bg-gray-50 text-gray-800 dark:bg-gray-900 dark:text-gray-100 min-h-screen">
    <NavBar />

    <main>
      <FadeIn>
        <section id="home" class="h-screen flex flex-col justify-center items-center text-center">
          <h1 class="text-5xl font-bold">Hello, I'm <span class="text-blue-500">Thomas</span></h1>
          <p class="mt-4 text-lg">
            <span class="block sm:inline">Aspiring Frontend Developer</span>
            <span class="hidden sm:inline"> | </span>
            <span class="block sm:inline">JavaScript • Tailwind • Vue</span>
          </p>
          <div class="mt-6 flex gap-3">
            <a
              href="#projects"
              class="px-6 py-3 bg-blue-500 text-white rounded-xl shadow hover:bg-blue-600 transition"
            >
              View My Work
            </a>
            <a
              href="https://drive.google.com/file/d/1-yK8nBv_zieB7ovcz2QbEPr1Q4zBmFed/view?usp=sharing"
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
        <section id="about" class="pt-16 max-w-5xl mx-auto text-center">
          <h2 class="text-3xl font-bold mb-6">About Me</h2>
          <p class="text-lg px-6 text-justify">
            A current Software Engineering student at Mae Fah Luang University with strong
            problem-solving abilities and a solid foundation in web technologies, including HTML,
            CSS, and JavaScript. Familiar with backend development using Node.js and Express, and
            eager to deepen expertise in full-stack development. Motivated to apply technical
            knowledge in real-world software engineering projects, while continuously learning from
            industry professionals.
          </p>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="education" class="pt-16">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Education</h2>
            <div class="space-y-6">
              <!-- Current Degree -->
              <div
                class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow border-l-4 border-blue-500"
              >
                <div class="flex items-start justify-between mb-4">
                  <div class="flex-1">
                    <div class="flex items-center mb-2">
                      <div class="w-3 h-3 bg-blue-500 rounded-full mr-3"></div>
                      <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                        B.Eng. in Software Engineering
                      </h3>
                    </div>
                    <p class="text-blue-600 dark:text-blue-400 font-medium mb-1">
                      Mae Fah Luang University
                    </p>
                    <p class="text-sm text-gray-500">Expected Graduation: 2026</p>
                  </div>
                  <span
                    class="px-3 py-1 text-xs font-medium bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full"
                  >
                    Current
                  </span>
                </div>
                <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                  <p class="text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">
                    Relevant coursework:
                  </p>
                  <div class="text-sm text-gray-600 dark:text-gray-400">
                    Software Engineering • Web Development • Application Development • Data
                    Structures & Algorithms • Object-Oriented Programming
                  </div>
                </div>
              </div>

              <!-- Previous Degree -->
              <div
                class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow border-l-4 border-gray-300 dark:border-gray-600"
              >
                <div class="flex items-start justify-between mb-4">
                  <div class="flex-1">
                    <div class="flex items-center mb-2">
                      <div class="w-3 h-3 bg-gray-400 rounded-full mr-3"></div>
                      <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                        B.A. in Business
                      </h3>
                    </div>
                    <p class="text-gray-600 dark:text-gray-400 font-medium mb-1">
                      Myanmar Institute of Theology
                    </p>
                    <p class="text-sm text-gray-500">2018 - 2023</p>
                  </div>
                  <span
                    class="px-3 py-1 text-xs font-medium bg-gray-100 dark:bg-gray-700 text-gray-600 dark:text-gray-400 rounded-full"
                  >
                    Completed
                  </span>
                </div>
                <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                  <p class="text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">
                    Relevant coursework:
                  </p>
                  <div class="text-sm text-gray-600 dark:text-gray-400">
                    Business Strategy • Entrepreneurship • Project Management • Sales • Human
                    Resource Management
                  </div>
                </div>
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
        <section id="projects" class="pt-12 pb-16 bg-gray-100 dark:bg-gray-800">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div style="--stagger: 0">
                <ProjectCard
                  title="My Portfolio"
                  description="This very site! Built with Vue 3 + TailwindCSS."
                  tech="Vue, Tailwind"
                  link="https://github.com/SawThomasMMK/my-portfolio.git"
                  image="/images/portfolioCover.png"
                  imageAlt="Screenshot of portfolio website"
                />
              </div>
            </div>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="experience" class="pt-16">
          <div class="max-w-5xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8">Experience</h2>
            <div class="space-y-6">
              <!-- Academic Presentation -->
              <div
                class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow border-l-4 border-green-500"
              >
                <div class="flex items-start justify-between mb-4">
                  <div class="flex-1">
                    <div class="flex items-center mb-2">
                      <div class="w-3 h-3 bg-green-500 rounded-full mr-3"></div>
                      <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                        Academic Presentation
                      </h3>
                    </div>
                    <p class="text-green-600 dark:text-green-400 font-medium mb-1">
                      RAG for lifestyle improvement — ECTI DAMT & NCON 2025
                    </p>
                    <p class="text-sm text-gray-500">February 2025</p>
                  </div>
                  <span
                    class="px-3 py-1 text-xs font-medium bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-full"
                  >
                    Conference
                  </span>
                </div>
                <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                  <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
                    Presented on "AI in Health and Tech" topic at the ECTI DAMT & NCON 2025
                    conference.
                  </p>
                  <a
                    href="https://www.canva.com/design/DAGXBD0k16o/_45eDbYvt7E3CJdcCgp6Ew/edit?utm_content=DAGXBD0k16o&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="inline-flex items-center text-sm text-green-600 dark:text-green-400 hover:text-green-700 dark:hover:text-green-300 transition-colors"
                  >
                    View Presentation →
                  </a>
                </div>
              </div>

              <!-- Teaching Experience -->
              <div
                class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow border-l-4 border-blue-500"
              >
                <div class="flex items-start justify-between mb-4">
                  <div class="flex-1">
                    <div class="flex items-center mb-2">
                      <div class="w-3 h-3 bg-blue-500 rounded-full mr-3"></div>
                      <h3 class="text-lg font-semibold text-gray-900 dark:text-white">Teacher</h3>
                    </div>
                    <p class="text-blue-600 dark:text-blue-400 font-medium mb-1">
                      Thoo Mweh Khee Migrant Learning Center
                    </p>
                    <p class="text-sm text-gray-500">June 2023 – July 2023</p>
                  </div>
                  <span
                    class="px-3 py-1 text-xs font-medium bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full"
                  >
                    Teaching
                  </span>
                </div>
                <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                  <ul class="space-y-2 text-sm">
                    <li class="flex items-start">
                      <span
                        class="w-1.5 h-1.5 bg-blue-500 rounded-full mr-3 mt-2 flex-shrink-0"
                      ></span>
                      <span class="text-gray-600 dark:text-gray-400">
                        Instructed and supervised students in Mathematics, Economics, and Computer
                        Basics
                      </span>
                    </li>
                    <li class="flex items-start">
                      <span
                        class="w-1.5 h-1.5 bg-blue-500 rounded-full mr-3 mt-2 flex-shrink-0"
                      ></span>
                      <span class="text-gray-600 dark:text-gray-400">
                        Collaborated with colleagues to ensure effective curriculum and student
                        engagement
                      </span>
                    </li>
                  </ul>
                </div>
              </div>

              <!-- Leadership Experience -->
              <div
                class="bg-white dark:bg-gray-800 rounded-xl p-6 shadow border-l-4 border-purple-500"
              >
                <div class="flex items-start justify-between mb-4">
                  <div class="flex-1">
                    <div class="flex items-center mb-2">
                      <div class="w-3 h-3 bg-purple-500 rounded-full mr-3"></div>
                      <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                        Youth Program President
                      </h3>
                    </div>
                    <p class="text-purple-600 dark:text-purple-400 font-medium mb-1">
                      Insein Myothit Karen Baptist Church
                    </p>
                    <p class="text-sm text-gray-500">June 2020 – June 2022</p>
                  </div>
                  <span
                    class="px-3 py-1 text-xs font-medium bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full"
                  >
                    Leadership
                  </span>
                </div>
                <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                  <ul class="space-y-2 text-sm">
                    <li class="flex items-start">
                      <span
                        class="w-1.5 h-1.5 bg-purple-500 rounded-full mr-3 mt-2 flex-shrink-0"
                      ></span>
                      <span class="text-gray-600 dark:text-gray-400">
                        Planned and organized worship service programs
                      </span>
                    </li>
                    <li class="flex items-start">
                      <span
                        class="w-1.5 h-1.5 bg-purple-500 rounded-full mr-3 mt-2 flex-shrink-0"
                      ></span>
                      <span class="text-gray-600 dark:text-gray-400">
                        Assigned tasks to volunteers and ensured timely completion
                      </span>
                    </li>
                    <li class="flex items-start">
                      <span
                        class="w-1.5 h-1.5 bg-purple-500 rounded-full mr-3 mt-2 flex-shrink-0"
                      ></span>
                      <span class="text-gray-600 dark:text-gray-400">
                        Coordinated with guest pastors and speakers for worship services
                      </span>
                    </li>
                    <li class="flex items-start">
                      <span
                        class="w-1.5 h-1.5 bg-purple-500 rounded-full mr-3 mt-2 flex-shrink-0"
                      ></span>
                      <span class="text-gray-600 dark:text-gray-400">
                        Collaborated with church leaders to assist in church activities
                      </span>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </section>
      </FadeIn>

      <FadeIn>
        <section id="contact" class="pt-16 pb-8 max-w-3xl mx-auto text-center">
          <h2 class="text-3xl font-bold mb-2">Contact Me</h2>
          <p class="mb-8 text-gray-600 dark:text-gray-300">
            I’d love to hear from you. Send a message and I’ll reply as soon as I can.
          </p>

          <FadeIn>
            <div class="px-4">
              <form
                action="https://formspree.io/f/mnnbyvnv"
                method="POST"
                class="text-left bg-white dark:bg-gray-800 p-6 md:p-8 rounded-xl shadow space-y-5"
              >
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                  <div>
                    <label for="name" class="block text-sm font-medium mb-1">Your name</label>
                    <input
                      id="name"
                      name="name"
                      type="text"
                      placeholder="Thomas"
                      required
                      class="w-full rounded-lg border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-900 px-4 py-2.5 text-gray-900 dark:text-gray-100 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-400"
                    />
                  </div>
                  <div>
                    <label for="email" class="block text-sm font-medium mb-1">Email address</label>
                    <input
                      id="email"
                      name="email"
                      type="email"
                      placeholder="you@example.com"
                      required
                      class="w-full rounded-lg border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-900 px-4 py-2.5 text-gray-900 dark:text-gray-100 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-400"
                    />
                  </div>
                </div>

                <div>
                  <label for="message" class="block text-sm font-medium mb-1">Message</label>
                  <textarea
                    id="message"
                    name="message"
                    rows="6"
                    placeholder="Tell me a bit about your project or question…"
                    required
                    class="w-full rounded-lg border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-900 px-4 py-2.5 text-gray-900 dark:text-gray-100 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-400"
                  ></textarea>
                </div>

                <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-3">
                  <label class="inline-flex items-center text-sm text-gray-600 dark:text-gray-300">
                    <input type="checkbox" name="consent" required class="mr-2 accent-blue-500" />
                    I consent to be contacted regarding my message.
                  </label>
                  <button
                    type="submit"
                    class="w-full sm:w-auto px-5 py-2.5 bg-blue-500 text-white rounded-lg hover:bg-blue-600 focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-400"
                  >
                    Send message
                  </button>
                </div>

                <input type="hidden" name="_subject" value="New message from portfolio" />
              </form>
            </div>
          </FadeIn>
          <div class="space-x-4 pt-8 text-center">
            <a
              href="https://mail.google.com/mail/?view=cm&fs=1&to=6531503181@lamduan.mfu.ac.th"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blue-600 dark:text-blue-400 hover:underline"
              >Email</a
            >
            <a
              href="https://github.com/SawThomasMMK"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blue-600 dark:text-blue-400 hover:underline"
              >GitHub</a
            >
            <a
              href="https://www.linkedin.com/in/saw-thomas-maung-maung-kyaw-78608b279/"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blue-600 dark:text-blue-400 hover:underline"
              >LinkedIn</a
            >
          </div>
        </section>
      </FadeIn>
    </main>

    <footer class="pb-6 text-center text-sm text-gray-500 dark:text-gray-400">
      © 2025 Saw Thomas Maung Maung Kyaw. Built with Vue & Tailwind.
    </footer>
  </div>
</template>

<script setup>
import NavBar from './components/AppNavbar.vue'
import ProjectCard from './components/ProjectCard.vue'
import FadeIn from './components/FadeIn.vue'
</script>
