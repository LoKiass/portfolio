<script setup>
import Navbar from "@/components/navbar/NavbarSection.vue";
import Header from "@/components/header/HeaderSection.vue";
import About from "@/components/about/AboutSection.vue";
import TechStack from "@/components/stack/TechStackSection.vue";
import ProjectSection from "@/components/project/ProjectSection.vue";
import FooterSection from "./components/footer/FooterSection.vue";
import ContactSection from "./components/contact/ContactSection.vue";
</script>

<template>
  <Navbar /> <!-- Navbar component -->
  <Header /> <!-- Header component -->
  <section id="About" class="scroll-mt-20">
    <About /> <!-- About component -->
  </section>
  <section id="TechStack" class="scroll-mt-20">
    <TechStack /> <!-- TechStack component -->
  </section>
  <section id="Projects" class="scroll-mt-20">
    <ProjectSection /> <!-- ProjectSection component -->
  </section>
  <section id ="Contact" class="scroll-mt-20">
    <ContactSection /> <!-- ContactSection component -->
  </section>
  <FooterSection /> <!-- FooterSection component -->
</template>

<style scoped>
</style>
