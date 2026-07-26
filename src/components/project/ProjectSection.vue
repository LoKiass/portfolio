<script setup>
import ProjectCard from './ProjectCard.vue'
const projects = [
  {
    title: 'Portfolio',
    description: 'Mon portfolio personnel pour présenter mes projets et compétences.',
    image: '/images/portfolio.png',
    type: 'Web Development',
    link: 'https://github.com/matteodiseurs/portfolio'
  },
  {
    title: 'Airsoft Pro Shop',
    description: 'Un site e-commerce pour la vente d\'équipements d\'airsoft, avec une analyse de marché, concurence, proto-persona et wireframes.',
    image: '/images/airsoft-pro-shop.png',
    type: 'E-commerce / Analyse',
    link: 'https://github.com/matteodiseurs/airsoft-pro-shop'
  },
  {
    title: 'Projet TicketMaster',
    description: 'Un système de ticket pour gérer les demandes de support, avec une interface utilisateur simple utilisant Twig, Boostrap, php & MySQl.',
    image: '/images/system-ticket.png',
    type: 'Web Development / Parcour académique',
    link: 'https://github.com/LoKiass/ProjetTicketIT',
  },
  {
    title: 'Examen Administration & Gestion de Base de Données Avancée',
    description: 'Un projet d\'examen pour la création d\'une base de données avancée, avec des requêtes SQL complexes et des relations entre les tables.',
    image: '/images/examendb.png',
    type: 'Database Design / PSQL / Parcour académique',
    link: 'https://github.com/LoKiass/EAFCSUDLUX2025-2026_EXAMENDB'
  }
]
</script>

<template>
  <section class="project-section py-12">
    <div class="container px-4 mx-15">
          <h2 class="bg-linear-to-r from-cyan-500 via-cyan-800 to-cyan-900 bg-clip-text text-transparent text-2xl md:text-4xl font-bold mb-8">
Projets</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ProjectCard
          v-for="(project, index) in projects"        
        :key="index"
        :title="project.title"
        :description="project.description"
        :image="project.image"
        :type="project.type"
        :link="project.link"
        />
      </div>
    </div>
  </section>
</template>