<script setup>
import '../assets/css/introduction.css';
import fotoLuiz from '../assets/fotos/Foto_Luiz.jpg';
const saudacao = new Date().getHours() < 12 ? 'Bom dia' : 'Olá';
</script>

<template>
    <section id="home" class="intro-section d-flex align-items-center min-vh-100 bg-white">
        <div class="container-md">
            <div class="row align-items-center">
                <div class="col-lg-7 text-center text-lg-start order-2 order-lg-1">
                    <span class="badge rounded-pill bg-primary mb-3 px-3 py-2 shadow-sm">
                        <i class="bi bi-geo-alt-fill me-2"></i>Manaus, Amazonas
                    </span>
                    <h1 class="display-3 fw-bold mb-3">
                        {{ saudacao }}, eu sou o <br>
                        <span class="text-primary">Luiz Felipe Neves</span>.
                    </h1>
                    <p class="lead text-dark mb-4">
                        Tenho 26 anos e sou um <strong>Desenvolvedor Full Stack</strong> apaixonado por transformar lógica em soluções digitais.
                    </p>
                    <p class="text-secondary mb-5 fs-6" style="max-width: 600px;">
                        Especialista no ecossistema <strong>PHP & Laravel</strong>, focado em construir sistemas robustos e escaláveis. Minha missão é resolver problemas complexos com código limpo e eficiente.
                    </p>
                    <div class="d-flex justify-content-center justify-content-lg-start gap-3">
                        <a href="#projetos" class="btn btn-primary btn-lg px-4 shadow">Ver Projetos</a>
                        <a href="https://github.com/LuizFelipe2023" target="_blank" class="btn btn-outline-dark btn-lg px-4">
                            <i class="bi bi-github me-2"></i>GitHub
                        </a>
                    </div>
                </div>
                <div class="col-lg-5 text-center order-1 order-lg-2 mb-5 mb-lg-0">
                    <div class="photo-wrapper p-2 d-inline-block rounded-circle shadow-lg bg-white border">
                        <img :src="fotoLuiz" alt="Foto do Luiz" class="img-fluid rounded-circle profile-img">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>

</style>