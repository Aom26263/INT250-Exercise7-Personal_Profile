<script setup>
import { ref } from 'vue'

const certs = [
  {
    title: 'Learn Bootstrap',
    focus: 'Responsive design and layout systems.',
    date: 'March 2026',
    img: new URL('../assets/Bootstrap.jpg', import.meta.url).href,
  },
  {
    title: 'Fundamentals of VueJS',
    focus: 'Reactivity, routing, and state management.',
    date: 'March 2026',
    img: new URL('../assets/Vue.js.jpg', import.meta.url).href,
  },
  {
    title: 'Learn Tailwind CSS',
    focus: 'Utility-first styling and modern UI.',
    date: 'March 2026',
    img: new URL('../assets/Tailwind.jpg', import.meta.url).href,
  },
]

const selected = ref(null)
const openModal = (cert) => { selected.value = cert }
const closeModal = () => { selected.value = null }
</script>

<template>
  <section id="activities" class="bg-white dark:bg-gray-900 transition-colors duration-300 py-16 sm:py-24">
    <div class="max-w-6xl mx-auto px-6 sm:px-16">

      <!-- Header -->
      <div class="mb-12 sm:mb-16">
        <p class="text-blue-600 text-xs font-bold tracking-widest uppercase mb-3">Credentials</p>
        <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 dark:text-white leading-tight">
          Experience &amp; Activities
        </h2>
      </div>

      <!-- Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-3 gap-5 sm:gap-6">
        <div
          v-for="cert in certs"
          :key="cert.title"
          class="group relative bg-slate-50 dark:bg-gray-800 border border-gray-100 dark:border-gray-700 rounded-2xl p-6 flex flex-col gap-5 hover:-translate-y-1 hover:shadow-xl hover:shadow-blue-500/10 hover:border-blue-200 dark:hover:border-blue-700 transition-all duration-300"
        >
          <!-- Certification badge + medal -->
          <div class="flex items-center justify-between">
            <span class="text-[10px] font-bold tracking-widest uppercase bg-blue-50 dark:bg-blue-950/60 text-blue-600 dark:text-blue-400 border border-blue-100 dark:border-blue-900 px-2.5 py-1 rounded-full">
              Certification
            </span>
            <div class="w-9 h-9 rounded-xl bg-blue-600 flex items-center justify-center shrink-0 group-hover:scale-110 transition-transform duration-200">
              <svg viewBox="0 0 24 24" class="w-4.5 h-4.5 text-white" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <circle cx="12" cy="8" r="6"/>
                <path d="M8.56 2.75c4.37 6.03 6.02 9.42 8.03 17.72m2.54-15.38c-3.72 4.35-8.94 5.66-16.88 5.85m19.5 1.9c-3.5-.93-6.63-.82-8.94 0-2.58.92-5.01 2.86-7.44 6.32"/>
              </svg>
            </div>
          </div>

          <!-- Title + focus -->
          <div class="flex flex-col gap-1.5 flex-1">
            <h3 class="text-base font-bold text-gray-900 dark:text-white leading-snug">{{ cert.title }}</h3>
            <p class="text-sm text-gray-500 dark:text-gray-400 leading-relaxed">{{ cert.focus }}</p>
          </div>

          <!-- Meta: Coursera + date -->
          <div class="flex items-center justify-between text-xs text-gray-400 dark:text-gray-500">
            <div class="flex items-center gap-1.5 font-semibold text-gray-500 dark:text-gray-400">
              <span class="w-4 h-4 rounded-full bg-blue-600 flex items-center justify-center text-white font-black text-[9px] shrink-0">C</span>
              Coursera
            </div>
            <div class="flex items-center gap-1">
              <svg viewBox="0 0 24 24" class="w-3 h-3" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <rect x="3" y="4" width="18" height="18" rx="2" ry="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/>
              </svg>
              {{ cert.date }}
            </div>
          </div>

          <!-- View Certificate button -->
          <button
            @click="openModal(cert)"
            class="flex items-center justify-center gap-2 w-full py-2.5 rounded-xl text-xs font-bold uppercase tracking-wider border-2 border-blue-600 text-blue-600 dark:text-blue-400 dark:border-blue-500 hover:bg-blue-600 hover:text-white dark:hover:bg-blue-600 dark:hover:text-white transition-all duration-200 cursor-pointer"
          >
            <svg viewBox="0 0 24 24" class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/>
            </svg>
            View Certificate
          </button>

        </div>
      </div>
    </div>
  </section>

  <!-- ── Modal ── -->
  <Teleport to="body">
    <Transition name="fade">
      <div
        v-if="selected"
        class="fixed inset-0 z-50 flex items-center justify-center p-4 sm:p-8 bg-black/70 backdrop-blur-sm"
        @click.self="closeModal"
      >
        <div class="relative bg-white dark:bg-gray-900 rounded-2xl shadow-2xl max-w-2xl w-full overflow-hidden">

          <!-- Modal header -->
          <div class="flex items-center justify-between px-5 py-4 border-b border-gray-100 dark:border-gray-800">
            <div>
              <p class="text-[10px] font-bold tracking-widest uppercase text-blue-600 mb-0.5">Certification</p>
              <h3 class="text-sm font-bold text-gray-900 dark:text-white">{{ selected.title }}</h3>
            </div>
            <button
              @click="closeModal"
              class="w-8 h-8 rounded-full flex items-center justify-center text-gray-400 hover:text-gray-900 dark:hover:text-white hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors duration-150 cursor-pointer"
            >
              <svg viewBox="0 0 24 24" class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
                <line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/>
              </svg>
            </button>
          </div>

          <!-- Certificate image -->
          <img :src="selected.img" :alt="selected.title" class="w-full object-contain max-h-[70vh]" />

        </div>
      </div>
    </Transition>
  </Teleport>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
