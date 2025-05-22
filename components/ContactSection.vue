<template>
  <section id="contact" class="py-20 md:py-32 relative">
    <div class="absolute inset-0 bg-slate-900/50"></div>
    <div class="container mx-auto px-4 relative z-10">
      <UiSectionHeading>Contact Me</UiSectionHeading>

      <div class="mt-16 grid md:grid-cols-1 gap-12">
        <div>
          <h3 class="text-2xl font-bold text-slate-50 mb-6">Let's Talk</h3>
          <p class="text-slate-300 mb-8">
            I'm currently available for freelance work or full-time positions.
            If you have a project that you want to get started, think you need
            my help with something, or just want to say hello, then get in
            touch.
          </p>

          <div class="space-y-4">
            <div class="flex items-center">
              <div
                class="w-12 h-12 rounded-full bg-slate-800 flex items-center justify-center mr-4"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-sky-400"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
              </div>
              <div>
                <div class="text-sm text-slate-400">Email</div>
                <a
                  href="mailto:sukitchowandee@gmail.com"
                  class="text-slate-200 hover:text-sky-400 transition-colors"
                  >sukitchowandee@gmail.com</a
                >
              </div>
            </div>

            <div class="flex items-center">
              <div
                class="w-12 h-12 rounded-full bg-slate-800 flex items-center justify-center mr-4"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-emerald-400"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                  />
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                  />
                </svg>
              </div>
              <div>
                <div class="text-sm text-slate-400">Location</div>
                <div class="text-slate-200">Samut Sakhon, Thailand</div>
              </div>
            </div>

            <div class="flex items-center">
              <div
                class="w-12 h-12 rounded-full bg-slate-800 flex items-center justify-center mr-4"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-emerald-400"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
                  />
                </svg>
              </div>
              <div>
                <div class="text-sm text-slate-400">Phone</div>
                <a
                  href="tel:+66858323487"
                  class="text-slate-200 hover:text-sky-400 transition-colors"
                >
                  +66 85 832 3487
                </a>
              </div>
            </div>

            <div class="flex items-center">
              <div
                class="w-12 h-12 rounded-full bg-slate-800 flex items-center justify-center mr-4"
              >
                <img
                  src="https://www.vectorlogo.zone/logos/line/line-icon.svg"
                  alt="Line"
                  class="h-5 w-5"
                />
              </div>
              <div>
                <div class="text-sm text-slate-400">Line ID</div>
                <div class="text-slate-200">sukitart</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Background animation elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div
        class="absolute top-1/3 right-1/4 w-96 h-96 bg-sky-500/20 rounded-full blur-3xl"
      ></div>
      <div
        class="absolute bottom-1/4 left-1/3 w-96 h-96 bg-emerald-500/20 rounded-full blur-3xl"
      ></div>
    </div>
  </section>
</template>

<script setup>
// SectionHeading component is imported automatically by Nuxt
</script>
