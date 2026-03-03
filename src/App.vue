<script setup>
import Navbar from './components/Navbar.vue';
import Introduction from './components/Introduction.vue';
import Habilidades from './components/Habilidades.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue'; 
import Footer from './components/Footer.vue';

import './assets/css/main.css';
</script>

<template>
  <Navbar />

  <main>
    <Introduction id="home" />

    <div class="py-5 bg-light">
      <Habilidades id="habilidades" />
    </div>

    <div class="py-5">
      <Projects id="projetos" />
    </div>

    <div class="py-5 bg-light border-top">
      <Contact id="contato" />
    </div>
  </main>

  <Footer />
</template>

<style>

</style>