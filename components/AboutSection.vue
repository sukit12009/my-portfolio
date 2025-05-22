<template>
  <section id="about" class="py-20 md:py-32 relative overflow-hidden">
    <div class="container mx-auto px-4">
      <UiSectionHeading>About Me</UiSectionHeading>

      <div class="grid md:grid-cols-2 gap-12 items-center mt-16 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Text Content -->
        <div class="order-2 md:order-1">
          <div class="space-y-6 text-slate-300 text-lg leading-relaxed">
            <p class="text-justify">
              Hi, my name is Sukit Chowandee, a passionate front-end developer
              with a strong foundation in computer science. I have hands-on
              experience building responsive user interfaces and bringing
              designs to life through modern web technologies.
            </p>

            <p class="text-justify">
              Currently, I'm expanding my skill set by self-learning back-end
              development. I enjoy tackling technical challenges and exploring
              new tools to create more complete and scalable solutions.
            </p>

            <p class="text-justify">
              I value teamwork, continuous learning, and clear communication. My
              goal is to grow into a full-stack developer while making a
              meaningful impact in every project I contribute to.
            </p>
          </div>

          <div class="mt-10">
            <UiBaseButton secondary href="/resume.pdf" target="_blank" class="group">
              <span class="flex items-center">
                <span>Download Resume</span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 ml-2 transform group-hover:translate-y-0.5 transition-transform duration-200"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"
                  />
                </svg>
              </span>
            </UiBaseButton>
          </div>
        </div>

        <!-- Image Container -->
        <div class="order-1 md:order-2 relative flex justify-center">
          <div class="relative z-10 w-1/2 max-w-md">
            <div class="relative pb-[125%] rounded-2xl overflow-hidden shadow-2xl shadow-slate-900/30 border-2 border-slate-700/50 transform transition-all duration-500 hover:scale-[1.02] hover:shadow-sky-500/20">
              <img 
                src="/images/profile.jpg" 
                alt="Sukit Chowandee" 
                class="absolute inset-0 w-full h-full object-cover"
                loading="lazy"
              />
            </div>
          </div>

          <!-- Decorative elements -->
          <div
            class="absolute -top-8 -right-8 w-32 h-32 bg-sky-500/20 rounded-full blur-3xl opacity-70"
            aria-hidden="true"
          ></div>
          <div
            class="absolute -bottom-12 -left-12 w-40 h-40 bg-emerald-500/20 rounded-full blur-3xl opacity-70"
            aria-hidden="true"
          ></div>
          <div class="absolute -z-10 inset-0 bg-gradient-to-tr from-slate-900/50 to-transparent rounded-2xl"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// SectionHeading component is imported automatically by Nuxt
</script>
