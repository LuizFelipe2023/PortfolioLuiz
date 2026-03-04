<script setup>
import { ref } from 'vue';
import '../assets/css/projects.css';
const projetos = ref([
    {
        id: 1,
        titulo: 'LaraKeep',
        subtitulo: 'Gerenciador de Notas Moderno',
        descricao: 'Inspirado no Google Keep, com reatividade extrema via Livewire 3 e isolamento de dados entre usuários (Multi-tenancy).',
        techs: ['Laravel 10', 'Livewire 3', 'MySQL', 'JavaScript'],
        linkGithub: 'https://github.com/LuizFelipe2023/LaraKeep',
        tipo: 'Full Stack / UX'
    },
    {
        id: 2,
        titulo: 'Dev Report',
        subtitulo: 'Sistema de Versionamento',
        descricao: 'Plataforma para controle de versões e documentos. Foco em relacionamentos complexos de banco de dados e gerenciamento de arquivos.',
        techs: ['PHP / Laravel', 'SQLite', 'Bootstrap', 'jQuery'],
        linkGithub: 'https://github.com/LuizFelipe2023/DevReport',
        tipo: 'Backend / Arquitetura'
    },
    {
        id: 3,
        titulo: 'Violator Landing Page',
        subtitulo: 'Thrash Until Death 🎸',
        descricao: 'Projeto educativo de interface para a banda Violator. Focado em UX para música, com carrossel de discografia e design responsivo.',
        techs: ['HTML5', 'CSS3', 'JavaScript ES6'],
        linkGithub: 'https://github.com/LuizFelipe2023/LandingPageViolator',
        tipo: 'Front-end / UI'
    },
    {
        id: 4,
        titulo: 'ShowTracker',
        subtitulo: 'Gestão de Séries & Filmes',
        descricao: 'CRUD moderno com interface Dark Mode. Inclui filtragem dinâmica por múltiplos géneros, upload de capas e interatividade SPA via Inertia.js.',
        techs: ['Laravel 11', 'Vue 3', 'InertiaJS', 'Tailwind CSS', 'MySQL'],
        linkGithub: 'https://github.com/LuizFelipe2023/ShowTracker',
        tipo: 'Full Stack / SPA'
    }
]);
</script>

<template>
    <section id="projetos" class="py-5 bg-white">
        <div class="container-md">
            <div class="row mb-5 text-center">
                <div class="col-12">
                    <span class="text-primary fw-bold text-uppercase tracking-wider small">Portfólio</span>
                    <h2 class="display-5 fw-bold text-dark">Projetos em Destaque</h2>
                    <div class="line mx-auto mb-3"></div>
                    <p class="text-muted">Projetos que demonstram minha evolução do Back-end ao Front-end.</p>
                </div>
            </div>

            <div class="row g-4 justify-content-center">
                <div v-for="projeto in projetos" :key="projeto.id" class="col-md-6 col-lg-4">
                    <div class="card h-100 shadow-sm border-0 project-card overflow-hidden">
                        <div class="card-header bg-dark d-flex gap-1 py-2 px-3 align-items-center">
                            <div class="dot bg-danger"></div>
                            <div class="dot bg-warning"></div>
                            <div class="dot bg-success"></div>
                            <span class="text-white-50 ms-2" style="font-size: 0.65rem; font-family: monospace;">
                                {{ projeto.titulo.replace(/\s+/g, '_').toLowerCase() }}.js
                            </span>
                        </div>

                        <div class="card-body p-4 bg-light d-flex flex-column">
                            <div class="mb-3">
                                <span class="badge bg-primary-subtle text-primary border border-primary-subtle mb-2">{{
                                    projeto.tipo }}</span>
                                <h4 class="fw-bold mb-1 text-dark">{{ projeto.titulo }}</h4>
                                <p class="text-secondary small fw-bold mb-0">{{ projeto.subtitulo }}</p>
                            </div>

                            <p class="card-text text-secondary mb-4 flex-grow-1" style="font-size: 0.9rem;">
                                {{ projeto.descricao }}
                            </p>

                            <div class="mb-4">
                                <div class="d-flex flex-wrap gap-2">
                                    <span v-for="tech in projeto.techs" :key="tech" class="badge-tech">
                                        {{ tech }}
                                    </span>
                                </div>
                            </div>

                            <a :href="projeto.linkGithub" target="_blank" class="btn btn-dark w-100 fw-bold mt-auto">
                                <i class="bi bi-github me-2"></i>Ver no GitHub
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
