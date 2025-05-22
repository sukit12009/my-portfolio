<template>
  <div
    class="bg-slate-800/50 rounded-lg overflow-hidden border border-slate-700/50 shadow-lg transform transition-all duration-500 hover:-translate-y-2 hover:shadow-xl"
  >
    <div class="relative pt-[56.25%] bg-slate-900/50">
      <div class="absolute inset-0 flex items-center justify-center p-4">
        <img
          :src="project.image"
          :alt="project.title"
          class="max-w-full max-h-full object-contain transition-transform duration-300 hover:scale-105"
        />
      </div>
      <div
        class="absolute inset-0 bg-gradient-to-t from-slate-900/90 via-slate-900/20 to-transparent opacity-70"
      ></div>
    </div>

    <div class="p-6">
      <h3 class="text-xl font-bold text-slate-50 mb-2">{{ project.title }}</h3>
      <p class="text-slate-400 mb-4">{{ project.description }}</p>

      <div class="flex flex-wrap gap-2 mb-6">
        <span
          v-for="tag in project.tags"
          :key="tag"
          class="px-2 py-1 text-xs rounded-full bg-slate-700 text-slate-300"
        >
          {{ tag }}
        </span>
      </div>

      <div class="flex space-x-3">
        <a
          :href="project.demoUrl"
          target="_blank"
          class="text-sky-400 hover:text-sky-300 transition-colors flex items-center"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-4 w-4 mr-1"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
            />
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"
            />
          </svg>
          <span>Live Demo</span>
        </a>
        <a
          :href="project.githubUrl"
          target="_blank"
          class="text-slate-400 hover:text-slate-300 transition-colors flex items-center"
        >
          <svg
            class="w-4 h-4 mr-1"
            fill="currentColor"
            viewBox="0 0 24 24"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
              clip-rule="evenodd"
            ></path>
          </svg>
          <span>Source Code</span>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  project: {
    type: Object,
    required: true,
  },
});
</script>
