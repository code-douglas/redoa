# redoa

# 📦 Sistema de Doações com IA e Autenticação

Projeto full stack com foco em doações de produtos, geração automática de descrições por inteligência artificial e autenticação completa. Desenvolvido como MVP com arquitetura MVC, ideal para portfólio.

---

## 📚 Funcionalidades

### 🧾 Cadastro e Autenticação
- Cadastro de usuário com:
  - Nome completo
  - Email
  - Telefone
  - Senha + confirmação
- Confirmação de email via token
- Login e autenticação via JWT
- Login automático após confirmação de email
- Proteção de rotas para usuários autenticados

### 🏠 Página Pública
- Home com listagem de produtos doados
- Exibição de imagem e título do produto
- Página de detalhes do produto (restrita a usuários logados)
  - Descrição completa
  - Telefone do doador (extraído do cadastro)

### 👤 Dashboard do Usuário
- **Informações Pessoais**
  - Visualizar nome e email
  - Editar telefone (refletido automaticamente nos produtos)

- **Gerenciar Produtos**
  - Ver lista de produtos que cadastrou
  - Editar título e descrição
  - Excluir produto doado

### 🤖 Integração com IA
- Ao subir imagem do produto, a IA gera:
  - Um título sugerido
  - Uma descrição coerente com a imagem
- IA via API gratuita (OpenAI ou alternativa)

---

## 🧱 Tecnologias Utilizadas

| Camada       | Tecnologias                          |
|--------------|--------------------------------------|
| Backend      | Node.js, Express                     |
| View Engine  | Handlebars                           |
| Banco de Dados | MongoDB Atlas                     |
| Autenticação | JWT                                  |
| Upload       | Multer                               |
| Email        | Nodemailer + SMTP (ex: Gmail)        |
| IA           | API OpenAI (GPT) ou alternativa      |

---

## ⚙️ Requisitos Técnicos

- Node.js 18+
- MongoDB Atlas (grátis)
- Conta para envio de emails (SMTP)
- Conta na OpenAI ou API similar (free tier)
- (Opcional) Docker para deploy local ou em nuvem

---

## 🗂 Estrutura de Diretórios (MVC)
```
📁 src
├── controllers/
├── models/
├── routes/
├── views/
│ ├── layouts/
│ └── partials/
├── middleware/
├── services/ # Integração com IA e envio de email
├── public/ # CSS, imagens e JS estático
└── uploads/ # Imagens dos produtos
```
---

## 🚀 Executando o Projeto

```bash
# Instale as dependências
npm install

# Inicie o servidor
npm start
```

## Configure variáveis de ambiente como:

```
MONGODB_URI

JWT_SECRET

EMAIL_USER

EMAIL_PASS

OPENAI_API_KEY
```

## 📌 Roadmap Futuro
Adicionar paginação e busca por produtos

Upload para Cloudinary ou outro storage

Interface administrativa para validação de doações

Internacionalização (i18n)

## 🧑‍💻 Autor
Desenvolvido por Douglas – projeto para portfólio.
