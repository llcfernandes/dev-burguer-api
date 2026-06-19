# 🍔 Dev Burguer API

> Backend de uma aplicação de hamburgueria desenvolvida durante o curso Dev Club.

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Node](https://img.shields.io/badge/node-ES%20Modules-green)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 📌 Sobre o projeto

API REST desenvolvida com foco em boas práticas de arquitetura backend.

O projeto segue o padrão **MVC** e está sendo construído com autenticação, validação de dados, controle de acesso e upload de arquivos.

---

## 🛠️ Stack

| Tecnologia | Uso |
| --- | --- |
| Node.js | Runtime |
| Express | Framework HTTP |
| PostgreSQL | Banco de dados relacional |
| Sequelize | ORM |
| Docker | Ambiente do banco de dados |
| Yup | Validação de dados |
| UUID | Geração de IDs únicos |

---

## ✅ O que já está implementado

- [x] Estrutura MVC
- [x] Conexão com banco via Docker + PostgreSQL
- [x] Migration da tabela de usuários
- [x] Criação de usuários com validação de dados (Yup)
- [x] Verificação de email duplicado
- [x] Resposta segura sem exposição de senha
- [x] Login de usuários

---

## 🚧 Em desenvolvimento

- [ ] Autenticação JWT
- [ ] Gestão de produtos
- [ ] Upload de imagem
- [ ] Controle de pedidos

---

## 📁 Estrutura do projeto

src/

├── app/

│   ├── controllers/

│   └── models/

├── config/

├── database/

│   └── migrations/

├── app.js

├── routes.js

└── server.js

---

Projeto desenvolvido por **Lucas Fernandes** durante o curso Dev Club.
