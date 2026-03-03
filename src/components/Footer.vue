<script setup>
import '../assets/css/footer.css';
</script>


<template>
  <footer class="bg-dark text-white pt-5 pb-4">
    <div class="container-md">
      <div class="row align-items-center">
        <div class="col-md-6 text-center text-md-start mb-4 mb-md-0">
          <h5 class="fw-bold">Luiz Felipe Frois Neves</h5>
          <p class="text-white-50 small mb-0">
            Desenvolvedor Full Stack especializado no ecossistema PHP & Laravel.<br>
            Construindo soluções robustas de ponta a ponta.
          </p>
        </div>

        <div class="col-md-6 text-center text-md-end">
          <div class="d-flex justify-content-center justify-content-md-end gap-3 mb-3">
            <a href="https://github.com/LuizFelipe2023" target="_blank" class="social-icon">
              <i class="bi bi-github"></i>
            </a>
            <a href="#" target="_blank" class="social-icon">
              <i class="bi bi-linkedin"></i>
            </a>
            <a href="mailto:seu-email@exemplo.com" class="social-icon">
              <i class="bi bi-envelope-fill"></i>
            </a>
          </div>
          <p class="text-white-50 small">
            &copy; {{ new Date().getFullYear() }} — Desenvolvido com <strong>Vue.js</strong> e <strong>Bootstrap</strong>.
          </p>
        </div>
      </div>

      <hr class="mt-4 border-secondary opacity-25">
      
      <div class="text-center">
        <span class="badge bg-secondary-subtle text-secondary fw-normal px-3">
          Status: Disponível para novos projetos
        </span>
      </div>
    </div>
  </footer>
</template>

