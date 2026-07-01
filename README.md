# 🍔 Dev Burguer API

API RESTful para gerenciamento completo de uma plataforma de pedidos para hamburgueria, desenvolvida com Node.js, Express, PostgreSQL e MongoDB.

O projeto simula a arquitetura utilizada em aplicações reais de e-commerce e delivery, implementando autenticação JWT, autorização por níveis de acesso, upload de imagens, relacionamento entre entidades, persistência híbrida de dados (SQL e NoSQL), arquitetura MVC e boas práticas de segurança.

![Node.js](https://img.shields.io/badge/Node.js-22.x-green)
![Express](https://img.shields.io/badge/Express-5.x-black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![MongoDB](https://img.shields.io/badge/MongoDB-NoSQL-green)
![Sequelize](https://img.shields.io/badge/Sequelize-ORM-blue)
![Mongoose](https://img.shields.io/badge/Mongoose-ODM-darkred)
![JWT](https://img.shields.io/badge/JWT-Authentication-orange)
![Status](https://img.shields.io/badge/Status-Backend%20Concluído-success)

---

# 🚀 Funcionalidades

## 👤 Gestão de usuários

- Cadastro de usuários
- Validação de dados com Yup
- Criptografia de senhas utilizando BCrypt
- Verificação de e-mail duplicado
- Login com autenticação JWT

---

## 🔐 Autenticação e autorização

- Login com JWT
- Middleware de autenticação
- Rotas protegidas
- Controle de acesso por nível de usuário (Admin/User)
- Sessões autenticadas via Bearer Token

---

## 🍔 Gestão de produtos

- Cadastro de produtos
- Atualização de produtos
- Listagem de produtos
- Upload de imagens
- Associação entre produtos e categorias
- Produtos em oferta
- URL virtual para imagens

---

## 🗂️ Gestão de categorias

- Cadastro de categorias
- Atualização de categorias
- Upload de imagem
- Listagem de categorias
- Validação de categorias duplicadas

---

## 🛒 Sistema de pedidos

- Criação de pedidos
- Persistência utilizando MongoDB
- Atualização do status do pedido
- Listagem de pedidos
- Associação automática entre usuário e pedido
- Busca automática dos produtos cadastrados no PostgreSQL
- Armazenamento apenas das informações necessárias no pedido

---

## 🔒 Segurança

- Hash de senhas com BCrypt
- JWT assinado
- Middleware de autenticação
- Middleware de administrador
- Validação completa de dados
- Proteção de rotas privadas

---

# 🏗️ Arquitetura

O projeto segue a arquitetura MVC, separando responsabilidades e facilitando manutenção, escalabilidade e reutilização de código.

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

Schemas (Mongoose)
        ↓
 MongoDB
```

---

# 🛠️ Tecnologias

## Backend

- Node.js
- Express

## Banco de dados

- PostgreSQL
- MongoDB

## ORM / ODM

- Sequelize
- Mongoose

## Segurança

- JWT
- BCrypt

## Upload de arquivos

- Multer

## Validação

- Yup

## Desenvolvimento

- Docker
- UUID
- Biome

---

# 📂 Estrutura

```text
src
│
├── app
│   ├── controllers
│   ├── middlewares
│   ├── models
│   └── schemas
│
├── config
│
├── database
│   └── migrations
│
├── uploads
│
├── app.js
├── routes.js
└── server.js
```

---

# 🔑 Fluxo de autenticação

```text
Login
   ↓
Validação das credenciais
   ↓
JWT
   ↓
Bearer Token
   ↓
Middleware
   ↓
Acesso às rotas protegidas
```

---

# 📦 Fluxo de pedidos

```text
Cliente envia produtos
          ↓
API recebe apenas ID e quantidade
          ↓
Produtos são buscados no PostgreSQL
          ↓
Pedido é montado no backend
          ↓
Pedido salvo no MongoDB
```

---

# 🖼️ Fluxo de upload

```text
Upload
   ↓
Multer
   ↓
UUID
   ↓
Uploads
   ↓
Path salvo
   ↓
URL virtual
   ↓
Frontend
```

---

# 📋 Endpoints

## Usuários

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| POST | /users | Cadastro de usuário |

---

## Sessões

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| POST | /sessions | Login |

---

## Produtos

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| POST | /products | Criar produto *(Admin)* |
| PUT | /products/:id | Atualizar produto *(Admin)* |
| GET | /products | Listar produtos |

---

## Categorias

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| POST | /categories | Criar categoria *(Admin)* |
| PUT | /categories/:id | Atualizar categoria *(Admin)* |
| GET | /categories | Listar categorias |

---

## Pedidos

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| POST | /orders | Criar pedido |
| PUT | /orders/:id | Atualizar status *(Admin)* |
| GET | /orders | Listar pedidos |

---

# 📌 Destaques técnicos

- Arquitetura MVC
- PostgreSQL para dados relacionais
- MongoDB para gerenciamento de pedidos
- Relacionamentos entre entidades com Sequelize
- Upload de imagens com Multer
- Autorização baseada em permissões
- Validação completa utilizando Yup
- API REST seguindo boas práticas de organização e escalabilidade

---

# 🚀 Próximas implementações

- Front-end completo em React
- Dashboard administrativo
- Paginação
- Filtros e pesquisa
- Exclusão de produtos e categorias
- Integração com serviço de pagamentos
- Deploy em ambiente cloud (Frontend + Backend + Banco)

---

# 👨‍💻 Autor

Desenvolvido por **Lucas Fernandes** durante a formação Full Stack do DevClub.

Este é meu principal projeto de backend até o momento e foi desenvolvido para simular a arquitetura de uma aplicação real de delivery, utilizando tecnologias amplamente adotadas pelo mercado e boas práticas de desenvolvimento de APIs REST.