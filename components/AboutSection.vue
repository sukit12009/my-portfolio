<template>
  <section id="about" class="py-20 md:py-32 relative overflow-hidden">
    <div class="container mx-auto px-4">
      <UiSectionHeading>About Me</UiSectionHeading>

      <div class="grid md:grid-cols-2 gap-12 items-center mt-16">
        <div class="order-2 md:order-1">
          <h3 class="text-2xl font-bold text-slate-50 mb-6">
            A passionate developer with a creative mindset
          </h3>

          <div class="space-y-4 text-slate-300">
            <p>
              Hello! I'm [Your Name], a software developer specializing in building exceptional digital experiences.
              I enjoy creating things that live on the internet, whether that be websites, applications, or anything in
              between.
            </p>

            <p>
              My interest in web development started back in 2012 when I decided to try editing custom Tumblr themes —
              turns out hacking together a custom reblog button taught me a lot about HTML & CSS!
            </p>

            <p>
              Fast-forward to today, and I've had the privilege of working at an advertising agency, a start-up, and a
              large corporation. My main focus these days is building accessible, inclusive products and digital
              experiences.
            </p>
          </div>

          <div class="mt-8">
            <UiBaseButton secondary href="/resume.pdf" target="_blank">
              <span class="flex items-center">
                <span>Download Resume</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
                </svg>
              </span>
            </UiBaseButton>
          </div>
        </div>

        <div class="order-1 md:order-2 relative">
          <div
            class="relative z-10 rounded-lg overflow-hidden shadow-xl shadow-slate-900/20 border border-slate-700/50 transform transition-transform hover:scale-[1.02] duration-500">
            <!-- <img src="/images/profile.jpg" alt="Your Name" class="w-full h-auto" /> -->
          </div>

          <!-- Decorative elements -->
          <div class="absolute -top-6 -right-6 w-24 h-24 bg-sky-500/20 rounded-full blur-xl"></div>
          <div class="absolute -bottom-10 -left-10 w-32 h-32 bg-emerald-500/20 rounded-full blur-xl"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// SectionHeading component is imported automatically by Nuxt
</script>