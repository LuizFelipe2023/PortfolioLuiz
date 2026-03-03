<script setup>
import '../assets/css/navbar.css';
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top shadow-sm">
    <div class="container-md">
      <a class="navbar-brand fw-bold" href="#">
        <span class="text-primary">&lt;</span> Luiz.dev <span class="text-primary">/&gt;</span>
      </a>

      <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto align-items-center">
          <li class="nav-item">
            <a class="nav-link px-3" href="#home">Início</a>
          </li>
          <li class="nav-item">
            <a class="nav-link px-3" href="#projetos">Projetos</a>
          </li>
          <li class="nav-item">
            <a class="nav-link px-3" href="#habilidades">Habilidades</a>
          </li>
          <li class="nav-item ms-lg-3">
            <a class="btn btn-outline-primary btn-sm px-4" href="#contato">
              Contatos
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
