<template>
  <section id="hero" class="min-h-screen flex items-center justify-center relative overflow-hidden">
    <div class="container mx-auto px-4 py-20 md:py-32 relative z-10">
      <div class="max-w-3xl mx-auto text-center">
        <h1 class="text-4xl md:text-6xl font-bold mb-6 text-slate-50">
          <span class="block">Hi, I'm <span class="text-sky-400">Sukit Chowandee</span></span>
          <span class="block mt-2">
            <UiTypewriterEffect :texts="[
              'Frontend Developer',
              'Backend Developer',
              'Full Stack Developer',
            ]" />
          </span>
        </h1>

        <p class="text-xl text-slate-300 mb-10 leading-relaxed">
          I build beautiful, responsive websites with modern technologies that
          help businesses grow and users smile.
        </p>

        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <UiBaseButton tag="a" primary href="#projects">View My Work</UiBaseButton>
          <UiBaseButton tag="a" secondary href="#contact">Contact Me</UiBaseButton>
        </div>

        <div class="mt-16 animate-bounce">
          <a href="#about" class="inline-block text-slate-400 hover:text-sky-400 transition-colors">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
              stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
            </svg>
          </a>
        </div>
      </div>
    </div>

    <!-- Background animation elements -->
    <div class="absolute inset-0 z-0">
      <div class="absolute top-20 left-10 w-64 h-64 bg-sky-500/10 rounded-full blur-3xl"></div>
      <div class="absolute bottom-20 right-10 w-80 h-80 bg-emerald-500/10 rounded-full blur-3xl"></div>
    </div>
  </section>
</template>

<script setup>
// TypewriterEffect component is imported automatically by Nuxt
</script>
