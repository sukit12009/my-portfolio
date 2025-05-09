<template>
  <section id="skills" class="py-20 md:py-32 relative">
    <div class="container mx-auto px-4">
      <UiSectionHeading>My Skills</UiSectionHeading>

      <div class="mt-16 grid md:grid-cols-2 gap-12">
        <!-- Hard Skills -->
        <div>
          <h3 class="text-2xl font-bold text-slate-50 mb-6 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 text-sky-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
            </svg>
            Hard Skills
          </h3>

          <div class="grid grid-cols-2 gap-4">
            <div v-for="skill in hardSkills" :key="skill.name"
              class="bg-slate-800/50 border border-slate-700/50 rounded-lg p-4 transform transition-all duration-300 hover:scale-105 hover:shadow-lg flex items-center">
              <div class="w-10 h-10 mr-3 flex items-center justify-center rounded-lg" 
                   :class="skill.type === 'frontend' ? 'bg-sky-400/20 text-sky-400' : 'bg-emerald-500/20 text-emerald-500'">
                <Icon :icon="skill.icon" class="w-6 h-6" />
              </div>
              <h4 class="text-lg font-medium text-slate-50">{{ skill.name }}</h4>
            </div>
          </div>
        </div>

        <!-- Soft Skills -->
        <div>
          <h3 class="text-2xl font-bold text-slate-50 mb-6 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 text-emerald-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
            </svg>
            Soft Skills
          </h3>

          <div class="grid grid-cols-2 gap-4">
            <div v-for="(skill, index) in softSkills" :key="index"
              class="bg-slate-800/50 border border-slate-700/50 rounded-lg p-4 transform transition-transform hover:scale-105 duration-300">
              <div class="text-lg font-medium text-slate-50 mb-2">
                {{ skill.name }}
              </div>
              <div class="text-sm text-slate-400">{{ skill.description }}</div>
            </div>
          </div>
        </div>
      </div>

      <div class="mt-16">
        <h3 class="text-2xl font-bold text-slate-50 mb-6 text-center">
          Technologies I Work With
        </h3>

        <div class="flex flex-wrap justify-center gap-8 mt-8">
          <UiTechIcon v-for="tech in technologies" :key="tech.name" :name="tech.name" :icon="tech.icon" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Icon } from '@iconify/vue';

// รวม frontend และ backend เป็น hardSkills
const hardSkills = [
  { name: 'JavaScript', icon: 'logos:javascript', type: 'frontend' },
  { name: 'Vue.js', icon: 'logos:vue', type: 'frontend' },
  { name: 'React', icon: 'logos:react', type: 'frontend' },
  { name: 'HTML/CSS', icon: 'logos:html-5', type: 'frontend' },
  { name: 'Tailwind CSS', icon: 'logos:tailwindcss-icon', type: 'frontend' },
  { name: 'TypeScript', icon: 'logos:typescript-icon', type: 'frontend' },
  { name: 'Node.js', icon: 'logos:nodejs', type: 'backend' },
  { name: 'Express', icon: 'logos:express', type: 'backend' },
  { name: 'MongoDB', icon: 'logos:mongodb', type: 'backend' },
  { name: 'RESTful APIs', icon: 'logos:postman', type: 'backend' },
  { name: 'GraphQL', icon: 'logos:graphql', type: 'backend' },
  { name: 'SQL', icon: 'logos:mysql', type: 'backend' }
];

const softSkills = [
  {
    name: "Problem Solving",
    description: "Analytical thinking and creative solutions",
  },
  { name: "Communication", description: "Clear and effective communication" },
  { name: "Teamwork", description: "Collaborative and supportive team player" },
  {
    name: "Time Management",
    description: "Efficient prioritization and organization",
  },
  {
    name: "Adaptability",
    description: "Quick to learn and adapt to new technologies",
  },
  {
    name: "Attention to Detail",
    description: "Meticulous and thorough approach",
  },
];

const technologies = [
  { name: "JavaScript", icon: "logos:javascript" },
  { name: "Vue.js", icon: "logos:vue" },
  { name: "React", icon: "logos:react" },
  { name: "Node.js", icon: "logos:nodejs" },
  { name: "Tailwind CSS", icon: "logos:tailwindcss-icon" },
  { name: "Git", icon: "logos:git-icon" },
  { name: "VS Code", icon: "logos:visual-studio-code" },
  { name: "Figma", icon: "logos:figma" },
];
</script>
