<script setup>
function smoothScrollTo(id) {
  const el = document.getElementById(id)
  if (!el) return

  const navbarHeight = 64
  const targetY = el.getBoundingClientRect().top + window.scrollY - navbarHeight
  const startY = window.scrollY
  const distance = targetY - startY
  const duration = 800
  let startTime = null

  function easeInOutCubic(t) {
    return t < 0.5 ? 4 * t * t * t : 1 - Math.pow(-2 * t + 2, 3) / 2
  }

  function step(timestamp) {
    if (!startTime) startTime = timestamp
    const elapsed = timestamp - startTime
    const progress = Math.min(elapsed / duration, 1)
    window.scrollTo(0, startY + distance * easeInOutCubic(progress))
    if (progress < 1) requestAnimationFrame(step)
  }

  requestAnimationFrame(step)
}
</script>

<template>
  <section id="hero" class="min-h-screen bg-slate-100 dark:bg-gray-950 flex items-center transition-colors duration-300 pt-16">
    <div class="max-w-6xl mx-auto px-6 sm:px-16 py-12 sm:py-0 w-full flex flex-col-reverse items-center gap-10 sm:flex-row sm:justify-between sm:gap-16">

      <div class="flex-1 text-center sm:text-left">
        <p class="text-blue-500 text-xs font-bold tracking-widest uppercase mb-4 sm:mb-5">
          Available for Hire
        </p>

        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight mb-3 text-gray-900 dark:text-white">
          Sorrawich <span class="text-blue-600">Prasopsub</span>
        </h1>

        <h2 class="text-lg sm:text-xl lg:text-2xl font-bold text-gray-800 dark:text-gray-200 mb-5 sm:mb-6">
          Full Stack Developer
        </h2>

        <p class="text-gray-500 dark:text-gray-400 text-sm sm:text-base leading-relaxed max-w-md mx-auto sm:mx-0 mb-8 sm:mb-10">
          Designing and building high-performance web applications with engineering
          precision and seamless user experiences.
        </p>

        <div class="flex gap-4 justify-center sm:justify-start">
          <a href="#projects" @click.prevent="smoothScrollTo('projects')" class="bg-blue-600 hover:bg-blue-700 active:bg-blue-800 text-white font-bold px-6 sm:px-8 py-2.5 sm:py-3 rounded-lg transition-all duration-200 cursor-pointer hover:shadow-lg hover:shadow-blue-500/40 hover:-translate-y-0.5 active:translate-y-0 text-sm sm:text-base">
            View My Work
          </a>
          <a href="#contact" @click.prevent="smoothScrollTo('contact')" class="border-2 border-gray-300 dark:border-gray-600 text-gray-800 dark:text-gray-200 font-bold px-6 sm:px-8 py-2.5 sm:py-3 rounded-lg transition-all duration-200 cursor-pointer bg-transparent hover:bg-gray-200 dark:hover:bg-gray-800 hover:border-gray-500 dark:hover:border-gray-400 hover:-translate-y-0.5 active:translate-y-0 text-sm sm:text-base">
            Get In Touch
          </a>
        </div>
      </div>

      <div class="relative shrink-0">
        <div class="w-64 h-72 sm:w-80 sm:h-96 lg:w-[380px] lg:h-[420px] rounded-3xl overflow-hidden bg-gray-700 dark:bg-gray-800">
          <img
            src="../assets/Image (8).jpg"
            alt="Sorrawich Prasopsub"
            class="w-full h-full object-cover object-top"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
