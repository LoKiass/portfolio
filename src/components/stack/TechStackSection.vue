<!-- TechStack.vue (Parent) -->
<script setup>
import TechCard from './TechCard.vue'

const img = (path) => `${import.meta.env.BASE_URL}images/${path}`

const categories = [
  {
    name: "Frontend",
    technos: [
      { name: "HTML", image: img("html-5.png") },
      { name: "CSS", image: img("css-3.png") },
      { name: "Vue.js", image: img("vue.png") },
      { name: "JavaScript", image: img("js.png") },
      { name: "Tailwind CSS", image: img("tailwind.png") },
      { name: "Twig", image: img("twig.png") }
    ]
  },
  {
    name: "Backend",
    technos: [
      { name: "Node.js", image: img("nodejs.png") },
      { name: "PHP", image: img("php.png") },
      { name: "C#", image: img("c-sharp.png") }
    ]
  },
  {
    name: "Database",
    technos: [
      { name: "MySQL", image: img("mysql.png") },
      { name: "PSQL", image: img("postgre.png") }
    ]
  },
  {
    name: "DevOps & Tools",
    technos: [
      { name: "PowerShell", image: img("terminal.png") },
      { name: "Git", image: img("git.png") },
      { name: "Linux", image: img("linux-platform.png") }
    ]
  }
];
</script>

<template>
  <h1 class="text-white text-6xl md:text-8xl font-bold text-center mb-10">Tech Stack</h1>
  <div class="tech-stack my-10 px-4 md:px-8 max-w-7xl m-10">
    <h2 class="bg-linear-to-r from-cyan-500 via-cyan-800 to-cyan-900 bg-clip-text text-transparent text-2xl md:text-4xl font-bold mb-8">
      Tech Stack
    </h2>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-start">
      <div v-for="category in categories" :key="category.name" class="category p-6 rounded-2xl bg-slate-900/40 border border-slate-800/80 backdrop-blur-sm">
        <h3 class="text-white text-lg md:text-xl font-semibold mb-4 border-b border-slate-800 pb-2">
          {{ category.name }}
        </h3>
        <div class="grid grid-cols-2 sm:grid-cols-3 gap-3">
          <TechCard v-for="tech in category.technos" :key="tech.name" :name="tech.name" :image="tech.image" />
        </div>
      </div>
    </div>
  </div>
</template>
