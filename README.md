# 🍔 Dev Burguer API

API RESTful para gerenciamento de usuários e produtos de uma hamburgueria, desenvolvida utilizando Node.js, Express e PostgreSQL.

O projeto aplica conceitos utilizados em aplicações reais, incluindo autenticação JWT, upload de imagens, arquitetura MVC, validação de dados, ORM, controle de acesso e boas práticas de segurança.

![Node.js](https://img.shields.io/badge/Node.js-22.x-green)
![Express](https://img.shields.io/badge/Express-5.x-black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![Sequelize](https://img.shields.io/badge/Sequelize-ORM-blue)
![JWT](https://img.shields.io/badge/JWT-Authentication-orange)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)

---

## 🚀 Principais funcionalidades

### 👤 Gestão de usuários

- Cadastro de usuários
- Validação de dados utilizando Yup
- Criptografia de senha com BCrypt
- Verificação de email duplicado
- Proteção contra exposição de senha

### 🔐 Autenticação

- Login com email e senha
- Geração de token JWT
- Expiração automática de sessão
- Middleware de autenticação
- Proteção de rotas privadas

### 🍔 Gestão de produtos

- Cadastro de produtos
- Listagem de produtos
- Upload de imagens com Multer
- Geração automática de URL para imagens
- Armazenamento local de arquivos

### 🛡️ Segurança

- Hash de senhas utilizando BCrypt
- Tokens JWT assinados
- Validação de credenciais
- Mensagens genéricas para evitar enumeração de usuários
- Controle de acesso por autenticação

---

## 🏗️ Arquitetura

O projeto segue o padrão MVC (Model-View-Controller), separando responsabilidades e facilitando manutenção e escalabilidade.

```text
Request
   ↓
Routes
   ↓
Middlewares
   ↓
Controllers
   ↓
Models (Sequelize)
   ↓
PostgreSQL
```

---

## 🛠️ Tecnologias utilizadas

### Backend

- Node.js
- Express
- Sequelize ORM
- PostgreSQL

### Segurança

- BCrypt
- JSON Web Token (JWT)

### Upload de Arquivos

- Multer

### Validação

- Yup

### Utilitários

- UUID
- Biome

### Ambiente

- Docker

---

## 📂 Estrutura do projeto

```text
src
│
├── app
│   ├── controllers
│   └── models
│
├── config
│
├── database
│   └── migrations
│
├── middlewares
│
├── uploads
│
├── app.js
├── routes.js
└── server.js
```

---

## 🔑 Fluxo de autenticação

```text
Usuário faz login
        ↓
API valida credenciais
        ↓
JWT é gerado
        ↓
Token é enviado ao cliente
        ↓
Cliente envia Bearer Token
        ↓
Middleware valida JWT
        ↓
Acesso liberado
```

---

## 🖼️ Fluxo de upload de imagens

```text
Imagem enviada
       ↓
Multer recebe arquivo
       ↓
UUID é gerado
       ↓
Arquivo salvo em uploads
       ↓
Path salvo no banco
       ↓
URL virtual criada pelo Sequelize
       ↓
Frontend consome a imagem
```

---

## 📋 Endpoints disponíveis

### Usuários

| Método | Rota | Descrição |
|----------|----------|----------|
| POST | /users | Criar usuário |

### Sessão

| Método | Rota | Descrição |
|----------|----------|----------|
| POST | /session | Realizar login |

### Produtos

| Método | Rota | Descrição |
|----------|----------|----------|
| POST | /products | Criar produto |
| GET | /products | Listar produtos |

> As rotas de produtos são protegidas por autenticação JWT.

---

## 🚧 Próximas implementações

- Categorias de produtos
- Controle de permissões (Admin/User)
- Atualização de produtos
- Remoção de produtos
- Sistema de pedidos
- Integração com frontend React
- Deploy em ambiente cloud

---

## 👨‍💻 Autor

Desenvolvido por **Lucas Fernandes** durante a formação Full Stack do DevClub.

📌 Projeto construído com foco em aprendizado de arquitetura backend, autenticação, segurança e desenvolvimento de APIs REST.