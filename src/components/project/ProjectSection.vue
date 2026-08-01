<script setup>
import ProjectCard from './ProjectCard.vue'

const img = (path) => `${import.meta.env.BASE_URL}images/${path}`

const projects = [
  {
    title: 'Portfolio',
    description: 'Mon portfolio personnel pour présenter mes projets et compétences.',
    image: img('portfolio.png'),
    type: 'Web Development',
    link: 'https://github.com/LoKiass/portfolio'
  },
  {
    title: 'Airsoft Pro Shop',
    description: 'Un site e-commerce pour la vente d\'équipements d\'airsoft, avec une analyse de marché, concurence, proto-persona et wireframes.',
    image: img('airsoft.png'),
    type: 'E-Buisness / Analyse',
    link: 'https://github.com/matteodiseurs/airsoft-pro-shop'
  },
  {
    title: 'Projet TicketMaster',
    description: 'Un système de ticket pour gérer les demandes de support, avec une interface utilisateur simple utilisant Twig, Boostrap, php & MySQl.',
    image: img('TicketSystem.png'),
    type: 'Web Development / Database Design',
    link: 'https://github.com/LoKiass/ProjetTicketIT',
  },
  {
    title: 'Examen Administration & Gestion de Base de Données Avancée',
    description: 'Un projet d\'examen pour la création d\'une base de données avancée, avec des requêtes SQL complexes et des relations entre les tables.',
    image: img('examendb.png'),
    type: 'Database Designs',
    link: 'https://github.com/LoKiass/EAFCSUDLUX2025-2026_EXAMENDB'
  }
]
</script>

<template>
  <section class="project-section py-12">
    <div class="container px-4 mx-auto">
      <h2 class="bg-linear-to-r from-cyan-500 via-cyan-800 to-cyan-900 bg-clip-text text-transparent text-2xl md:text-4xl font-bold mb-8">
        Projets
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
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