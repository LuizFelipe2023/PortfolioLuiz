<script setup>
const coreStack = [
  { name: 'PHP 8+', level: 'Especialista', icon: 'bi-code-slash', color: '#777bb4' },
  { name: 'Laravel', level: 'Especialista', icon: 'bi-lightning-fill', color: '#ff2d20' },
  { name: 'MySQL', level: 'Domínio', icon: 'bi-database-fill', color: '#00758f' }
];

const techStack = [
  { name: 'JavaScript', level: 'Intermediário', icon: 'bi-filetype-js' },
  { name: 'Vue.js', level: 'Básico/Desenrola', icon: 'bi-patch-check' },
  { name: 'Docker', level: 'Básico/Ambiente', icon: 'bi-box-seam' },
  { name: 'Linux', level: 'Básico/Terminal', icon: 'bi-terminal' },
  { name: 'Bootstrap', level: 'Intermediário', icon: 'bi-bootstrap' },
  { name: 'HTML/CSS', level: 'Intermediário', icon: 'bi-layout-text-sidebar' }
];

import '../assets/css/habilidades.css';
</script>

<template>
  <section id="habilidades" class="py-5 bg-white">
    <div class="container-md">
      <div class="row mb-5 text-center">
        <div class="col-12">
          <h2 class="fw-bold">Stack Tecnológico</h2>
          <div class="line mx-auto mb-3"></div>
          <p class="text-muted">Minha especialidade é no ecossistema PHP, mas possuo versatilidade para atuar em todo o fluxo de desenvolvimento.</p>
        </div>
      </div>

      <div class="row g-4 mb-5 justify-content-center">
        <div v-for="skill in coreStack" :key="skill.name" class="col-md-4">
          <div class="card h-100 border-0 shadow-sm skill-card-main p-4">
            <div class="d-flex align-items-center">
              <i class="bi fs-1 me-3" :class="skill.icon" :style="{ color: skill.color }"></i>
              <div>
                <h4 class="fw-bold mb-0">{{ skill.name }}</h4>
                <small class="text-primary fw-bold text-uppercase" style="font-size: 0.7rem;">Especialidade</small>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="row g-3">
        <div v-for="skill in techStack" :key="skill.name" class="col-6 col-md-4 col-lg-2">
          <div class="card h-100 border p-3 text-center skill-card-secondary">
            <i class="bi fs-3 mb-2" :class="skill.icon"></i>
            <h6 class="fw-bold mb-1 small">{{ skill.name }}</h6>
            <div class="progress" style="height: 4px;">
              <div class="progress-bar" role="progressbar" 
                   :style="{ width: skill.level.includes('Básico') ? '40%' : '70%' }"></div>
            </div>
            <small class="text-muted mt-2" style="font-size: 0.65rem;">{{ skill.level }}</small>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

