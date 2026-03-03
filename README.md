# 🚀 Luiz.dev | Portfólio Pessoal

Projeto de portfólio moderno desenvolvido com **Vue 3** e **Vite**, focado em uma interface limpa e funcionalidade de contato direto via e-mail.

## 🛠 Tecnologias
* **Vue 3** (Composition API)
* **Vite** (Build Tool)
* **Bootstrap 5** (Layout e Componentes)
* **EmailJS** (Serviço de envio de e-mail)

## 📧 Funcionalidades de Contato
O formulário de contato integrado ao **EmailJS** permite:
- Envio de mensagens com Nome, E-mail e Assunto.
- Feedback em tempo real com alertas do Bootstrap (Sucesso/Erro).
- Opção de fechar (dismiss) as mensagens de status.
- Scroll suave da Navbar diretamente para a seção de contato.

## ⚙️ Configuração

### 1. Variáveis de Ambiente (`.env`)
Crie um arquivo `.env` na raiz do projeto:
```env
VITE_EMAILJS_SERVICE_ID=seu_service_id
VITE_EMAILJS_TEMPLATE_ID=seu_template_id
VITE_EMAILJS_PUBLIC_KEY=sua_public_key

```

### 2. Comandos de Execução

```sh
# Instalar dependências
npm install

# Rodar projeto (Development)
npm run dev

# Gerar Build (Production)
npm run build

```

## 📂 Estrutura Principal

* `Navbar.vue`: Navegação com âncora para `#contato`.
* `Contact.vue`: Lógica de validação e envio via EmailJS.
* `main.js`: Configurações globais e importação do Bootstrap.

---

**Desenvolvido por Luiz Felipe** 🚀

```
