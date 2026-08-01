<script setup>
import Navbar from "@/components/navbar/NavbarSection.vue";
import Header from "@/components/header/HeaderSection.vue";
import About from "@/components/about/AboutSection.vue";
import TechStack from "@/components/stack/TechStackSection.vue";
import ProjectSection from "@/components/project/ProjectSection.vue";
import FooterSection from "./components/footer/FooterSection.vue";
</script>

<template>
  <Navbar /> <!-- Navbar component -->
  <Header /> <!-- Header component -->
  <About /> <!-- About component -->
  <TechStack /> <!-- TechStack component -->
  <ProjectSection /> <!-- ProjectSection component -->
  <FooterSection/>
</template>

<style scoped>
</style>
