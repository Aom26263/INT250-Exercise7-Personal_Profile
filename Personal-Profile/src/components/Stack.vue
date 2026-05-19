<script setup>
const techStack = [
  {
    label: 'JavaScript',
    viewBox: '0 0 24 24',
    path: `<rect x="3" y="3" width="18" height="18" rx="3"/><text x="50%" y="62%" dominant-baseline="middle" text-anchor="middle" fill="currentColor" font-size="7.5" font-weight="800" font-family="monospace" stroke="none">JS</text>`
  },
  {
    label: 'Vue.js',
    viewBox: '0 0 24 24',
    path: `<path d="M12 3L2 20h4.5L12 10l5.5 10H22L12 3z"/><path d="M7.5 20h9" stroke-width="0"/>`
  },
  {
    label: 'Node.js',
    viewBox: '0 0 24 24',
    path: `<polyline points="5 17 5 12 10 7"/><line x1="12" y1="17" x2="19" y2="17"/>`
  },
  {
    label: 'MySQL',
    viewBox: '0 0 24 24',
    path: `<ellipse cx="12" cy="6" rx="8" ry="3"/><path d="M4 6v6c0 1.66 3.58 3 8 3s8-1.34 8-3V6"/><path d="M4 12v6c0 1.66 3.58 3 8 3s8-1.34 8-3v-6"/>`
  },
  {
    label: 'Tailwind<br/>CSS',
    viewBox: '0 0 24 24',
    path: `<path d="M6.5 8C7.5 5 9.5 3.5 12 4c3.5.5 4 3.5 5.5 4C19 8.5 20.5 7 21 6M3 14c1-3 3-4.5 5.5-4C12 10.5 12.5 13.5 14 14c1.5.5 3-1 3.5-2"/>`
  },
  {
    label: 'AWS /<br/>Vercel',
    viewBox: '0 0 24 24',
    path: `<path d="M4 17c0 0-1.5-3 2-5 0-4 3-7 6-6 1.5-3 6-3 7.5 1C22 7.5 23 10 21.5 13L20 17z"/><path d="M9 17l3-7 3 7"/><line x1="10.5" y1="14" x2="13.5" y2="14"/>`
  },
]

const designTools = [
  {
    label: 'GitHub',
    viewBox: '0 0 24 24',
    path: `<path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>`
  },
  {
    label: 'Userflow',
    viewBox: '0 0 24 24',
    path: `<rect x="2" y="2" width="6" height="4" rx="1"/><rect x="16" y="2" width="6" height="4" rx="1"/><rect x="9" y="18" width="6" height="4" rx="1"/><path d="M5 6v3a3 3 0 0 0 3 3h8a3 3 0 0 0 3-3V6"/><line x1="12" y1="12" x2="12" y2="18"/>`
  },
  {
    label: 'Figma',
    viewBox: '0 0 24 24',
    path: `<path d="M5 5.5A3.5 3.5 0 0 1 8.5 2H12v7H8.5A3.5 3.5 0 0 1 5 5.5z"/><path d="M12 2h3.5a3.5 3.5 0 1 1 0 7H12V2z"/><path d="M12 12.5a3.5 3.5 0 1 1 7 0 3.5 3.5 0 0 1-7 0z"/><path d="M5 12.5A3.5 3.5 0 0 1 8.5 9H12v7H8.5A3.5 3.5 0 0 1 5 12.5z"/><path d="M5 19.5A3.5 3.5 0 0 1 8.5 16H12v3.5a3.5 3.5 0 1 1-7 0z"/>`
  },
  {
    label: 'User<br/>Research',
    viewBox: '0 0 24 24',
    path: `<circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/><path d="M11 8a3 3 0 1 0 0 6"/>`
  },
  {
    label: 'Usability<br/>Testing',
    viewBox: '0 0 24 24',
    path: `<polyline points="9 11 12 14 22 4"/><path d="M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11"/>`
  },
]

const softSkills = [
  {
    label: 'Problem Solving',
    viewBox: '0 0 24 24',
    path: `<circle cx="12" cy="12" r="10"/><path d="M9.09 9a3 3 0 0 1 5.83 1c0 2-3 3-3 3"/><line x1="12" y1="17" x2="12.01" y2="17"/>`
  },
  {
    label: 'Design Thinking',
    viewBox: '0 0 24 24',
    path: `<line x1="12" y1="2" x2="12" y2="6"/><path d="M12 6a6 6 0 0 1 6 6c0 2.5-1.5 4.5-3.5 5.5V19a1 1 0 0 1-1 1h-3a1 1 0 0 1-1-1v-1.5C7.5 16.5 6 14.5 6 12a6 6 0 0 1 6-6z"/><line x1="10" y1="21" x2="14" y2="21"/>`
  },
  {
    label: 'Collaboration',
    viewBox: '0 0 24 24',
    path: `<path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/>`
  },
  {
    label: 'Communication',
    viewBox: '0 0 24 24',
    path: `<path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>`
  },
  {
    label: 'Empathy',
    viewBox: '0 0 24 24',
    path: `<path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/>`
  },
  {
    label: 'Adaptability',
    viewBox: '0 0 24 24',
    path: `<polyline points="23 4 23 10 17 10"/><polyline points="1 20 1 14 7 14"/><path d="M3.51 9a9 9 0 0 1 14.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0 0 20.49 15"/>`
  },
]
</script>

<template>
  <section id="stack" class="bg-slate-50 dark:bg-gray-950 transition-colors duration-300 py-16 sm:py-24">
    <div class="max-w-6xl mx-auto px-6 sm:px-16">

      <!-- Header -->
      <div class="mb-12 sm:mb-16">
        <p class="text-blue-600 text-xs font-bold tracking-widest uppercase mb-3">What I bring</p>
        <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 dark:text-white leading-tight">
          Skills &amp; Expertise
        </h2>
      </div>

      <div class="flex flex-col gap-12 sm:gap-16">

        <!-- ── Technical Stack ── -->
        <div>
          <div class="flex items-center gap-3 mb-6 sm:mb-8">
            <span class="w-1 h-5 bg-blue-600 rounded-full shrink-0"></span>
            <h3 class="text-xs font-bold tracking-widest uppercase text-gray-500 dark:text-gray-400">Technical Stack</h3>
          </div>
          <div class="grid grid-cols-3 sm:grid-cols-6 gap-3 sm:gap-4">
            <div
              v-for="tech in techStack"
              :key="tech.label"
              class="group bg-white dark:bg-gray-900 border border-gray-100 dark:border-gray-800 rounded-2xl py-6 sm:py-8 flex flex-col items-center gap-3 cursor-default hover:border-blue-300 dark:hover:border-blue-700 hover:shadow-lg hover:shadow-blue-500/10 hover:-translate-y-0.5 transition-all duration-200"
            >
              <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-xl bg-blue-50 dark:bg-blue-950/60 flex items-center justify-center group-hover:bg-blue-100 dark:group-hover:bg-blue-900/60 transition-colors duration-200">
                <svg
                  :viewBox="tech.viewBox"
                  class="w-5 h-5 sm:w-6 sm:h-6 text-blue-600"
                  fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"
                  v-html="tech.path"
                />
              </div>
              <span class="text-xs font-semibold text-gray-600 dark:text-gray-300 text-center leading-tight px-1" v-html="tech.label" />
            </div>
          </div>
        </div>

        <!-- ── Design & Tools ── -->
        <div>
          <div class="flex items-center gap-3 mb-6 sm:mb-8">
            <span class="w-1 h-5 bg-purple-500 rounded-full shrink-0"></span>
            <h3 class="text-xs font-bold tracking-widest uppercase text-gray-500 dark:text-gray-400">Design &amp; Tools</h3>
          </div>
          <div class="grid grid-cols-3 sm:grid-cols-5 gap-3 sm:gap-4">
            <div
              v-for="tool in designTools"
              :key="tool.label"
              class="group bg-white dark:bg-gray-900 border border-gray-100 dark:border-gray-800 rounded-2xl py-6 sm:py-8 flex flex-col items-center gap-3 cursor-default hover:border-purple-300 dark:hover:border-purple-700 hover:shadow-lg hover:shadow-purple-500/10 hover:-translate-y-0.5 transition-all duration-200"
            >
              <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-xl bg-purple-50 dark:bg-purple-950/60 flex items-center justify-center group-hover:bg-purple-100 dark:group-hover:bg-purple-900/60 transition-colors duration-200">
                <svg
                  :viewBox="tool.viewBox"
                  class="w-5 h-5 sm:w-6 sm:h-6 text-purple-600 dark:text-purple-400"
                  fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"
                  v-html="tool.path"
                />
              </div>
              <span class="text-xs font-semibold text-gray-600 dark:text-gray-300 text-center leading-tight px-1" v-html="tool.label" />
            </div>
          </div>
        </div>

        <!-- ── Soft Skills ── -->
        <div>
          <div class="flex items-center gap-3 mb-6 sm:mb-8">
            <span class="w-1 h-5 bg-emerald-500 rounded-full shrink-0"></span>
            <h3 class="text-xs font-bold tracking-widest uppercase text-gray-500 dark:text-gray-400">Soft Skills</h3>
          </div>
          <div class="flex flex-wrap gap-3">
            <div
              v-for="skill in softSkills"
              :key="skill.label"
              class="group flex items-center gap-2.5 bg-white dark:bg-gray-900 border border-gray-100 dark:border-gray-800 rounded-full pl-3 pr-5 py-2.5 cursor-default hover:border-emerald-300 dark:hover:border-emerald-700 hover:shadow-md hover:shadow-emerald-500/10 hover:-translate-y-0.5 transition-all duration-200"
            >
              <div class="w-7 h-7 rounded-full bg-emerald-50 dark:bg-emerald-950/60 flex items-center justify-center shrink-0 group-hover:bg-emerald-100 dark:group-hover:bg-emerald-900/60 transition-colors duration-200">
                <svg
                  :viewBox="skill.viewBox"
                  class="w-3.5 h-3.5 text-emerald-600 dark:text-emerald-400"
                  fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                  v-html="skill.path"
                />
              </div>
              <span class="text-sm font-semibold text-gray-700 dark:text-gray-200 whitespace-nowrap">{{ skill.label }}</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped></style>
