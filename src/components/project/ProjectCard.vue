<script setup>
const props = defineProps({
  title: String,
  description: String,
  image: String,
  type: String,
  link: String
});
</script>

<template>
  <div class="project-card p-6 rounded-2xl bg-slate-900/40 border border-slate-800/80 backdrop-blur-sm">
    <img :src="image" :alt="title" class="w-full h-48 object-cover rounded mb-4" />
    <h3 class="text-white text-lg md:text-xl font-semibold mb-2">{{ title }}</h3>
    <h4 class="text-cyan-400 text-sm md:text-base font-medium mb-2">{{ type }}</h4>
    <p class="text-gray-400 mb-4">{{ description }}</p>
    <a :href="link" target="_blank" rel="noopener noreferrer" class="text-blue-400 hover:underline transition">Voir le projet</a>
  </div>
</template>