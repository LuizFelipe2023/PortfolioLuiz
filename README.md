
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

## 📧 Contact Workflow
O sistema de contato elimina a necessidade de um servidor backend:
1.  **Validação:** Frontend valida os campos em tempo real via HTML5/Vue.
2.  **Envio:** O `Contact.vue` utiliza o SDK do EmailJS para disparar o e-mail via SMTP/API do Google.
3.  **Feedback:** Alertas dinâmicos do Bootstrap notificam o sucesso ou erro, com opção de fechamento manual.



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

## 📂 Project Highlights

* `Navbar.vue`: Navegação inteligente com âncoras (`#contato`) e scroll suave.
* `Contact.vue`: Lógica encapsulada com tratamento de estados (loading, success, error).
* `Assets`: CSS modularizado para garantir a identidade visual do Luiz.dev.

