<script setup></script>

<template>
  <section id="projects" class="bg-slate-50 dark:bg-gray-950 transition-colors duration-300 py-16 sm:py-24">
    <div class="max-w-6xl mx-auto px-6 sm:px-16">

      <!-- Header -->
      <div class="mb-12 sm:mb-16">
        <p class="text-blue-600 text-xs font-bold tracking-widest uppercase mb-3">What I've built</p>
        <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 dark:text-white leading-tight">Featured Projects</h2>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 sm:gap-8">

        <!-- ── Card 1: Kinya Medication Care ── -->
        <div class="bg-white dark:bg-gray-900 rounded-2xl overflow-hidden border border-gray-100 dark:border-gray-800 hover:shadow-xl hover:shadow-blue-500/5 hover:-translate-y-0.5 transition-all duration-300 flex flex-col">
          <div class="relative">
            <img
              src="../assets/Screenshot 2026-05-18 134115.png"
              class="w-full h-48 sm:h-56 object-cover object-top"
              alt="Kinya Medication Care"
            />
            <span class="absolute top-3 left-3 bg-blue-600 text-white text-[10px] font-bold tracking-widest uppercase px-2.5 py-1 rounded-full">
              Healthcare
            </span>
          </div>

          <div class="px-5 sm:px-6 py-5 flex flex-col flex-1 gap-4">

            <!-- Title + Role -->
            <div>
              <h3 class="text-base sm:text-lg font-bold text-gray-900 dark:text-white mb-1">
                Kinya Medication Care
              </h3>
              <p class="text-xs font-semibold text-blue-600 dark:text-blue-400 uppercase tracking-wide">
                Lead Full Stack Developer &amp; UI Designer
              </p>
            </div>

            <!-- Description -->
            <p class="text-sm text-gray-500 dark:text-gray-400 leading-relaxed">
              A full-stack healthcare management platform designed to support medication tracking,
              adherence monitoring, health analytics, and real-time patient management through an
              intuitive and modern dashboard experience.
            </p>

            <!-- Technologies -->
            <div>
              <p class="text-[10px] font-bold tracking-widest uppercase text-gray-400 dark:text-gray-500 mb-2">Technologies</p>
              <div class="flex flex-wrap gap-1.5">
                <span v-for="tech in ['Vue.js', 'Tailwind CSS', 'Figma', 'JavaScript']" :key="tech"
                  class="text-[11px] font-semibold bg-blue-50 dark:bg-blue-950/60 text-blue-700 dark:text-blue-300 border border-blue-100 dark:border-blue-900 rounded-md px-2 py-0.5">
                  {{ tech }}
                </span>
              </div>
            </div>

            <!-- Key Features -->
            <div>
              <p class="text-[10px] font-bold tracking-widest uppercase text-gray-400 dark:text-gray-500 mb-2">Key Features</p>
              <div class="flex flex-wrap gap-1.5">
                <span v-for="tag in ['User Research', 'Responsive Design', 'Design System', 'Accessibility']" :key="tag"
                  class="text-[11px] font-semibold bg-emerald-50 dark:bg-emerald-950/60 text-emerald-700 dark:text-emerald-300 border border-emerald-100 dark:border-emerald-900 rounded-md px-2 py-0.5">
                  {{ tag }}
                </span>
              </div>
            </div>

            <!-- Links -->
            <div class="flex gap-5 mt-auto pt-1">
              <a href="https://int-250-g06-foodie-kinya.vercel.app/" target="_blank"
                class="flex items-center gap-1.5 text-xs font-bold text-blue-600 dark:text-blue-400 uppercase tracking-wider hover:underline">
                <svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M8 6H6a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2v-2M16 2h6v6M10 14L22 2"/></svg>
                Live Demo
              </a>
              <a href="https://github.com/pxkrwit/INT250-G06-Foodie-Kinya.git" target="_blank"
                class="flex items-center gap-1.5 text-xs font-bold text-blue-600 dark:text-blue-400 uppercase tracking-wider hover:underline">
                <svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
                GitHub
              </a>
            </div>

          </div>
        </div>

        <!-- ── Card 2: COMBO & BOMB ── -->
        <div class="bg-white dark:bg-gray-900 rounded-2xl overflow-hidden border border-gray-100 dark:border-gray-800 hover:shadow-xl hover:shadow-purple-500/5 hover:-translate-y-0.5 transition-all duration-300 flex flex-col">
          <div class="relative">
            <img
              src="../assets/Screenshot 2026-05-18 135203.png"
              class="w-full h-48 sm:h-56 object-cover object-top"
              alt="COMBO & BOMB"
            />
            <span class="absolute top-3 left-3 bg-purple-600 text-white text-[10px] font-bold tracking-widest uppercase px-2.5 py-1 rounded-full">
              Game
            </span>
          </div>

          <div class="px-5 sm:px-6 py-5 flex flex-col flex-1 gap-4">

            <!-- Title + Role -->
            <div>
              <h3 class="text-base sm:text-lg font-bold text-gray-900 dark:text-white mb-1">
                COMBO &amp; BOMB
              </h3>
              <p class="text-xs font-semibold text-purple-600 dark:text-purple-400 uppercase tracking-wide">
                Game Logic Developer &amp; UI/UX Designer
              </p>
            </div>

            <!-- Description -->
            <p class="text-sm text-gray-500 dark:text-gray-400 leading-relaxed">
              A tactical line-connecting and block-exploding game featuring five progressively
              difficult stages. Players progress from a basic 4×4 practice grid to a high-stakes
              8×8 "Hell" mode filled with 14 bombs, requiring precise strategy to clear each level.
            </p>

            <!-- Technologies -->
            <div>
              <p class="text-[10px] font-bold tracking-widest uppercase text-gray-400 dark:text-gray-500 mb-2">Technologies</p>
              <div class="flex flex-wrap gap-1.5">
                <span v-for="tech in ['Vue.js', 'Tailwind CSS', 'Figma', 'JavaScript']" :key="tech"
                  class="text-[11px] font-semibold bg-purple-50 dark:bg-purple-950/60 text-purple-700 dark:text-purple-300 border border-purple-100 dark:border-purple-900 rounded-md px-2 py-0.5">
                  {{ tech }}
                </span>
              </div>
            </div>

            <!-- Key Features -->
            <div>
              <p class="text-[10px] font-bold tracking-widest uppercase text-gray-400 dark:text-gray-500 mb-2">Key Features</p>
              <div class="flex flex-wrap gap-1.5">
                <span v-for="tag in ['Game UI', 'Accessibility', 'Responsive Design']" :key="tag"
                  class="text-[11px] font-semibold bg-amber-50 dark:bg-amber-950/60 text-amber-700 dark:text-amber-300 border border-amber-100 dark:border-amber-900 rounded-md px-2 py-0.5">
                  {{ tag }}
                </span>
              </div>
            </div>

            <!-- Links -->
            <div class="flex gap-5 mt-auto pt-1">
              <a href="https://github.com/pxkrwit/Box-Battles.git" target="_blank"
                class="flex items-center gap-1.5 text-xs font-bold text-purple-600 dark:text-purple-400 uppercase tracking-wider hover:underline">
                <svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
                GitHub
              </a>
            </div>

          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped></style>
