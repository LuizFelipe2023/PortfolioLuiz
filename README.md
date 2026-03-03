# 🚀 Luiz.dev | Personal Portfolio

[![Vue.js](https://img.shields.io/badge/Vue.js-3.x-4fc08d?logo=vue.js)](https://vuejs.org/)
[![Vite](https://img.shields.io/badge/Vite-Latest-646cff?logo=vite)](https://vitejs.dev/)
[![EmailJS](https://img.shields.io/badge/EmailJS-Integrated-ffaa00?logo=mail.dot.ru)](https://www.emailjs.com/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952b3?logo=bootstrap)](https://getbootstrap.com/)

Portfólio moderno e responsivo focado em performance e conversão, utilizando **Vue 3** com a **Composition API**.

## 🛠️ Tech Stack
* **Core:** Vue 3 + Vite
* **UI/UX:** Bootstrap 5 + Bootstrap Icons
* **Communication:** EmailJS (Direct Client-side Emailing)
* **Deployment:** Vercel / Netlify / GitHub Pages

## 🖥️ Estrutura do Projeto
O portfólio está dividido em seções estratégicas para uma melhor experiência do usuário:

* **Navbar:** Navegação inteligente com links internos e scroll suave.
* **Hero / Introdução:** Apresentação profissional e call-to-action inicial.
* **Habilidades:** Showcase técnico das ferramentas e linguagens dominadas.
* **Projetos:** Galeria de trabalhos realizados com links e descrições.
* **Formulário de Contato:** Sistema funcional integrado ao **EmailJS** para envio de mensagens direto ao meu e-mail.
* **Footer:** Encerramento com links sociais e créditos do desenvolvedor.

## 📧 Fluxo de Contato (Serverless)
1.  **Validação:** Frontend valida os campos via HTML5 e reatividade do Vue.
2.  **Envio:** O componente `Contact.vue` utiliza o SDK do EmailJS para disparar o e-mail sem necessidade de backend próprio.
3.  **Feedback:** Alertas dinâmicos do Bootstrap notificam sucesso ou erro com opção de fechamento manual.



## ⚙️ Setup & Installation

### 1. Environment Variables
Crie um arquivo `.env` na raiz do projeto:
```env
VITE_EMAILJS_SERVICE_ID=seu_service_id
VITE_EMAILJS_TEMPLATE_ID=seu_template_id
VITE_EMAILJS_PUBLIC_KEY=sua_public_key

```

### 2. Quick Start

```bash
# Instalar dependências
npm install

# Iniciar servidor de desenvolvimento (HMR)
npm run dev

# Build para produção
npm run build

```

---

**Developed with ❤️ by [Luiz Felipe**](https://github.com/LuizFelipe2023)

```

