<template>
  <header
    class="fixed w-full bg-slate-800/80 backdrop-blur-sm z-50 transition-all duration-300"
    :class="{ 'shadow-lg shadow-slate-900/20': scrolled }"
  >
    <div class="container mx-auto px-4 py-4 flex justify-between items-center">
      <div class="text-xl font-bold text-sky-400">
        <span class="mr-2 text-slate-50">ART</span>Portfolio
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex space-x-8">
        <a
          v-for="item in navItems"
          :key="item.id"
          :href="`#${item.id}`"
          class="text-slate-200 hover:text-sky-400 transition-colors duration-300"
        >
          {{ item.label }}
        </a>
      </nav>

      <!-- Mobile Navigation Toggle -->
      <button
        @click="mobileMenuOpen = !mobileMenuOpen"
        class="md:hidden text-slate-200"
      >
        <span v-if="!mobileMenuOpen">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
          </svg>
        </span>
        <span v-else>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </span>
      </button>
    </div>

    <!-- Mobile Navigation Menu -->
    <div v-if="mobileMenuOpen" class="md:hidden bg-slate-800 shadow-lg">
      <div class="container mx-auto px-4 py-4">
        <nav class="flex flex-col space-y-4">
          <a
            v-for="item in navItems"
            :key="item.id"
            :href="`#${item.id}`"
            @click="mobileMenuOpen = false"
            class="text-slate-200 hover:text-sky-400 transition-colors duration-300 py-2"
          >
            {{ item.label }}
          </a>
        </nav>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const scrolled = ref(false);
const mobileMenuOpen = ref(false);

const navItems = [
  { id: "hero", label: "Home" },
  { id: "about", label: "About" },
  { id: "projects", label: "Projects" },
  { id: "skills", label: "Skills" },
  { id: "contact", label: "Contact" },
];

const checkScroll = () => {
  scrolled.value = window.scrollY > 20;
};

onMounted(() => {
  window.addEventListener("scroll", checkScroll);
  checkScroll();
});

onUnmounted(() => {
  window.removeEventListener("scroll", checkScroll);
});
</script>
