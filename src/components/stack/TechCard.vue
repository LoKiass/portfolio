<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  image: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="flex flex-col items-center gap-4">
    <img :src="image" :alt="name" class="w-24 h-24 object-cover hover:scale-110 transition-transform duration-300" />
    <h3 class="text-white text-lg font-semibold">{{ name }}</h3>
  </div>
</template>
