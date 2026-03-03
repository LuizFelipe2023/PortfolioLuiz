<script setup>
import { ref } from 'vue';
import emailjs from '@emailjs/browser';
import '../assets/css/contact.css';

const nome = ref('');
const email = ref('');
const assunto = ref('');
const mensagem = ref('');
const status = ref({ tipo: '', msg: '' });

const enviarContato = async () => {
  status.value = { tipo: 'info', msg: 'Enviando...' };

  const templateParams = {
    nome: nome.value,
    email: email.value,
    assunto: assunto.value,
    mensagem: mensagem.value,
  };

  try {
    await emailjs.send(
      import.meta.env.VITE_EMAILJS_SERVICE_ID,
      import.meta.env.VITE_EMAILJS_TEMPLATE_ID,
      templateParams,
      import.meta.env.VITE_EMAILJS_PUBLIC_KEY
    );

    status.value = { tipo: 'success', msg: 'Mensagem enviada com sucesso!' };
    
    nome.value = email.value = assunto.value = mensagem.value = '';

  } catch (e) {
    console.error("Erro ao enviar:", e);
    status.value = { tipo: 'danger', msg: 'Erro ao processar sua solicitação.' };
  }
};
</script>

<template>
  <section id="contato" class="py-5 bg-white">
    <div class="container-md py-5">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="card border-0 shadow-lg p-4 p-md-5 rounded-4">
            <h2 class="fw-bold text-center mb-4">Mande uma mensagem 🚀</h2>
            
            <div v-if="status.msg" 
                 :class="`alert alert-${status.tipo} alert-dismissible fade show border-0 shadow-sm`" 
                 role="alert">
              <i class="bi" :class="status.tipo === 'success' ? 'bi-check-circle-fill' : 'bi-exclamation-triangle-fill'"></i>
              <span class="ms-2">{{ status.msg }}</span>
              <button type="button" class="btn-close" @click="status.msg = ''"></button>
            </div>

            <form @submit.prevent="enviarContato">
              <div class="row g-3">
                <div class="col-md-6">
                  <label class="form-label small fw-bold">Seu Nome</label>
                  <input v-model="nome" type="text" class="form-control form-control-lg bg-light border-0" required>
                </div>
                <div class="col-md-6">
                  <label class="form-label small fw-bold">Seu melhor E-mail</label>
                  <input v-model="email" type="email" class="form-control form-control-lg bg-light border-0" required>
                </div>
                <div class="col-12">
                  <label class="form-label small fw-bold">Assunto</label>
                  <input v-model="assunto" type="text" class="form-control form-control-lg bg-light border-0" required>
                </div>
                <div class="col-12">
                  <label class="form-label small fw-bold">Como posso te ajudar?</label>
                  <textarea v-model="mensagem" rows="4" class="form-control form-control-lg bg-light border-0" required></textarea>
                </div>
                <div class="col-12 text-center mt-4">
                  <button type="submit" class="btn btn-primary btn-lg px-5 w-100 shadow-sm fw-bold">
                    Enviar para o Luiz
                  </button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

