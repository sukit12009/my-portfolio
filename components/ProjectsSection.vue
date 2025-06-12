<template>
  <section id="projects" class="py-20 md:py-32 relative overflow-hidden">
    <!-- Background animation elements -->
    <div class="absolute inset-0 -z-10 overflow-hidden">
      <div
        class="absolute top-1/4 left-1/4 w-96 h-96 bg-sky-500/5 rounded-full blur-3xl"
      ></div>
      <div
        class="absolute bottom-1/3 right-1/3 w-96 h-96 bg-emerald-500/5 rounded-full blur-3xl"
      ></div>
    </div>

    <div class="container mx-auto px-4 relative z-10">
      <UiSectionHeading>My Projects</UiSectionHeading>

      <div class="mt-16 grid md:grid-cols-2 lg:grid-cols-2 gap-8">
        <UiProjectCard
          v-for="project in projects"
          :key="project.id"
          :project="project"
        />
      </div>

      <div class="mt-16 text-center">
        <UiBaseButton
          primary
          href="https://github.com/sukit12009"
          target="_blank"
          tag="a"
        >
          <span class="flex items-center justify-center">
            <svg
              class="w-5 h-5 mr-2"
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
            <span>See More on GitHub</span>
          </span>
        </UiBaseButton>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  // {
  //   id: 1,
  //   title: "Chula Meeting Booking",
  //   description:
  //     "A meeting room booking system with user authentication, date/room selection, and booking details input.",
  //   image: "/images/chula-meeting-booking-demo.jpg",
  //   tags: ["Next.js", "Tailwind CSS", "MongoDB"],
  //   demoUrl: "https://chula-meeting-booking.vercel.app/",
  //   githubUrl: "https://github.com/sukit12009/chula-meeting-booking",
  // },
  {
    id: 2,
    title: "Todo List Frontend",
    description:
      "A lightweight web app to help users create, track, and complete their to-do tasks with ease.",
    image: "/images/to-do-list-web-demo.jpg",
    tags: ["ReactJS", "Tailwind CSS"],
    demoUrl: "https://to-do-list-web-beryl.vercel.app/",
    githubUrl: "https://github.com/sukit12009/to-do-list-web",
  },
  {
    id: 3,
    title: "Todo List Backend",
    description:
      "A simple RESTful API for managing a to-do list with tasks that can be created, viewed, updated, and deleted.",
    image: "/images/to-do-list-api-demo.jpg",
    tags: ["Go", "Swagger", "PostgreSQL"],
    demoUrl: "https://to-do-list-api-am59.onrender.com/swagger/index.html",
    githubUrl: "https://github.com/sukit12009/to-do-list-api",
  },
];
</script>
