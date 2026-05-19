<script setup>
import { ref, reactive } from 'vue'

const form = reactive({ name: '', email: '', subject: '', message: '' })
const submitted = ref(false)

function handleSubmit() {
  submitted.value = true
  setTimeout(() => { submitted.value = false }, 3000)
  form.name = ''
  form.email = ''
  form.subject = ''
  form.message = ''
}

const socials = [
  {
    label: 'Email',
    value: 'rom26263@gmail.com',
    href: 'mailto:rom26263@gmail.com',
    path: `<rect x="2" y="4" width="20" height="16" rx="3"/><polyline points="2,4 12,13 22,4"/>`,
  },
  {
    label: 'GitHub',
    value: 'github.com/Aom26263',
    href: 'https://github.com/Aom26263',
    path: `<path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>`,
  },
  {
    label: 'Instagram',
    value: '@axmsz_p',
    href: 'https://www.instagram.com/axmsz_p',
    path: `<rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" fill="currentColor" stroke="none"/>`,
  },
  {
    label: 'Facebook',
    value: 'sorrawich.prasopsub',
    href: 'https://www.facebook.com/sorrawich.prasopsub',
    path: `<circle cx="12" cy="12" r="10"/><path d="M15.5 8H13a1 1 0 0 0-1 1v3H9v3h3v7h3v-7h2.5l.5-3H15V9"/>`,
  },
]

const inputBase = 'w-full rounded-xl px-4 py-3 text-sm text-gray-900 dark:text-white bg-gray-50 dark:bg-gray-800 border border-gray-200 dark:border-gray-700 placeholder-gray-400 dark:placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all duration-200'
</script>

<template>
  <section id="contact" class="bg-slate-50 dark:bg-gray-950 transition-colors duration-300 py-16 sm:py-24">
    <div class="max-w-6xl mx-auto px-6 sm:px-16">

      <!-- Header -->
      <div class="mb-12 sm:mb-16">
        <p class="text-blue-600 text-xs font-bold tracking-widest uppercase mb-3">Let's connect</p>
        <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 dark:text-white leading-tight">Get In Touch</h2>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 gap-10 sm:gap-16 items-start">
        <div class="flex flex-col gap-8">
          <p class="text-gray-500 dark:text-gray-400 text-sm sm:text-base leading-relaxed">
            Have a vision for your next digital product? Let's build something exceptional together.
            Reach out via the form or any of my platforms below.
          </p>

          <div class="flex flex-col gap-4">
            <a
              v-for="s in socials"
              :key="s.label"
              :href="s.href"
              target="_blank"
              class="group flex items-center gap-4 p-4 rounded-2xl bg-white dark:bg-gray-900 border border-gray-100 dark:border-gray-800 hover:border-blue-300 dark:hover:border-blue-700 hover:shadow-md hover:shadow-blue-500/10 hover:-translate-y-0.5 transition-all duration-200"
            >
              <div class="w-10 h-10 rounded-xl bg-blue-50 dark:bg-blue-950/60 flex items-center justify-center shrink-0 group-hover:bg-blue-100 dark:group-hover:bg-blue-900/60 transition-colors duration-200">
                <svg viewBox="0 0 24 24" class="w-5 h-5 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" v-html="s.path" />
              </div>
              <div class="min-w-0">
                <p class="text-[10px] font-bold tracking-widest uppercase text-gray-400 dark:text-gray-500 mb-0.5">{{ s.label }}</p>
                <p class="text-sm font-semibold text-gray-700 dark:text-gray-200 truncate">{{ s.value }}</p>
              </div>
              <svg viewBox="0 0 24 24" class="w-4 h-4 text-gray-300 dark:text-gray-600 group-hover:text-blue-500 ml-auto shrink-0 transition-colors duration-200" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <polyline points="9 18 15 12 9 6"/>
              </svg>
            </a>
          </div>
        </div>

        <div class="bg-white dark:bg-gray-900 border border-gray-100 dark:border-gray-800 rounded-2xl p-6 sm:p-8">

          <Transition name="slide">
            <div v-if="submitted" class="flex items-center gap-3 bg-emerald-50 dark:bg-emerald-950/60 border border-emerald-200 dark:border-emerald-800 text-emerald-700 dark:text-emerald-300 rounded-xl px-4 py-3 mb-6 text-sm font-semibold">
              <svg viewBox="0 0 24 24" class="w-4 h-4 shrink-0" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
              Message sent! I'll get back to you soon.
            </div>
          </Transition>

          <form @submit.prevent="handleSubmit" novalidate class="flex flex-col gap-5">
            <div class="flex flex-col gap-1.5">
              <label class="text-xs font-bold tracking-wide text-gray-500 dark:text-gray-400 uppercase">Full Name</label>
              <input
                v-model="form.name"
                type="text"
                placeholder="Sorrawich Prasopsub"
                required
                :class="inputBase"
              />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-xs font-bold tracking-wide text-gray-500 dark:text-gray-400 uppercase">Email Address</label>
              <input
                v-model="form.email"
                type="email"
                placeholder="you@example.com"
                required
                :class="inputBase"
              />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-xs font-bold tracking-wide text-gray-500 dark:text-gray-400 uppercase">Subject</label>
              <input
                v-model="form.subject"
                type="text"
                placeholder="Project collaboration, freelance..."
                required
                :class="inputBase"
              />
            </div>

            <div class="flex flex-col gap-1.5">
              <label class="text-xs font-bold tracking-wide text-gray-500 dark:text-gray-400 uppercase">Message</label>
              <textarea
                v-model="form.message"
                rows="5"
                placeholder="Tell me about your project..."
                required
                :class="inputBase + ' resize-none'"
              />
            </div>

            <button
              type="submit"
              class="flex items-center justify-center gap-2 w-full py-3 rounded-xl bg-blue-600 hover:bg-blue-700 active:bg-blue-800 text-white text-sm font-bold tracking-wide transition-all duration-200 hover:shadow-lg hover:shadow-blue-500/30 hover:-translate-y-0.5 active:translate-y-0 cursor-pointer"
            >
              <svg viewBox="0 0 24 24" class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                <line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/>
              </svg>
              Send Message
            </button>

          </form>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: all 0.3s ease;
}
.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}
</style>
