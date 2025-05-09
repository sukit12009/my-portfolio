<template>
  <section id="projects" class="py-20 md:py-32 bg-slate-900/50 relative">
    <div class="container mx-auto px-4">
      <UiSectionHeading>My Projects</UiSectionHeading>

      <div class="mt-16 grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <UiProjectCard v-for="project in projects" :key="project.id" :project="project" />
      </div>

      <div class="mt-16 text-center">
        <UiBaseButton primary href="https://github.com/yourusername" target="_blank">
          <span class="flex items-center justify-center">
            <svg class="w-5 h-5 mr-2" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path fill-rule="evenodd"
                d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
                clip-rule="evenodd"></path>
            </svg>
            <span>See More on GitHub</span>
          </span>
        </UiBaseButton>
      </div>
    </div>

    <!-- Background animation elements -->
    <div class="absolute inset-0 z-0 overflow-hidden">
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-sky-500/5 rounded-full blur-3xl"></div>
      <div class="absolute bottom-1/3 right-1/3 w-96 h-96 bg-emerald-500/5 rounded-full blur-3xl"></div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    id: 1,
    title: "E-commerce Platform",
    description:
      "A full-featured online store with shopping cart, user authentication, and payment processing.",
    image: "/images/projects/ecommerce.jpg",
    tags: ["Vue.js", "Node.js", "MongoDB", "Stripe"],
    demoUrl: "https://example.com",
    githubUrl: "https://github.com/yourusername/ecommerce",
  },
  {
    id: 2,
    title: "Task Management App",
    description:
      "A productivity application for managing tasks, projects, and team collaboration.",
    image: "/images/projects/taskapp.jpg",
    tags: ["React", "Firebase", "Tailwind CSS"],
    demoUrl: "https://example.com",
    githubUrl: "https://github.com/yourusername/taskapp",
  },
  {
    id: 3,
    title: "Weather Dashboard",
    description:
      "Real-time weather information with forecast data and interactive maps.",
    image: "/images/projects/weather.jpg",
    tags: ["JavaScript", "API Integration", "Chart.js"],
    demoUrl: "https://example.com",
    githubUrl: "https://github.com/yourusername/weather",
  },
  {
    id: 4,
    title: "Portfolio Website",
    description:
      "A responsive portfolio website built with modern web technologies.",
    image: "/images/projects/portfolio.jpg",
    tags: ["Vue.js", "Nuxt.js", "Tailwind CSS"],
    demoUrl: "https://example.com",
    githubUrl: "https://github.com/yourusername/portfolio",
  },
  {
    id: 5,
    title: "Blog Platform",
    description:
      "A content management system for creating and publishing blog posts.",
    image: "/images/projects/blog.jpg",
    tags: ["Next.js", "GraphQL", "Markdown"],
    demoUrl: "https://example.com",
    githubUrl: "https://github.com/yourusername/blog",
  },
  {
    id: 6,
    title: "Social Media Dashboard",
    description:
      "Analytics dashboard for tracking social media performance across platforms.",
    image: "/images/projects/social.jpg",
    tags: ["Vue.js", "D3.js", "REST API"],
    demoUrl: "https://example.com",
    githubUrl: "https://github.com/yourusername/social",
  },
];
</script>
