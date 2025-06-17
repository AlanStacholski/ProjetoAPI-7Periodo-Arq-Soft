
```markdown
# 📘 ProjetoAPSarqSoftware

API RESTful construída com Node.js, Express e MongoDB, utilizando princípios sólidos de Arquitetura de Software. Este projeto simula um backend robusto e escalável para gerenciamento de **usuários**, **autores** e **postagens**.

---

## 🎯 Objetivo Acadêmico

Este projeto foi desenvolvido como parte da disciplina de Arquitetura de Software, com o objetivo de aplicar conceitos práticos como:

- Arquitetura em múltiplas camadas
- Princípios SOLID
- Inversão de dependência (services → repositories)
- Separação de responsabilidades
- Utilização de middlewares, DTOs e Swagger

---

## 🚀 Tecnologias Utilizadas

| Tecnologia     | Finalidade                              |
|----------------|------------------------------------------|
| **Node.js**    | Ambiente de execução JavaScript          |
| **Express**    | Framework web minimalista                |
| **MongoDB**    | Banco de dados NoSQL                     |
| **Mongoose**   | ODM para modelagem dos dados             |
| **Swagger**    | Documentação da API                      |
| **Dotenv**     | Variáveis de ambiente                    |
| **Nodemon**    | Hot reload durante o desenvolvimento     |

---

## 🧠 Estrutura de Pastas

```

ProjetoAPSarqSoftware/
│
├── src/
│   ├── config/                # Configurações globais (Mongo, JWT, Swagger)
│   ├── controllers/           # Lógica das requisições HTTP
│   ├── dtos/                  # Objetos de transferência de dados
│   ├── middleware/            # Middlewares (ex: autenticação)
│   ├── models/                # Modelos Mongoose (Author, Post, User)
│   ├── repositories/          # Camada de acesso a dados
│   ├── routes/                # Definição das rotas da API
│   └── services/              # Lógica de negócio entre controller ↔ repo
│
├── app.js                     # Configuração do app Express
├── server.js                  # Ponto de entrada do servidor
├── package.json
└── README.md

````

---

## 📦 Instalação e Execução

### ✅ Pré-requisitos:
- Node.js instalado
- MongoDB local ou MongoDB Atlas
- Postman ou Insomnia para testar

### 💻 Passos:

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/ProjetoAPSarqSoftware.git
cd ProjetoAPSarqSoftware

# Instale as dependências
npm install

# Configure suas variáveis de ambiente
touch .env
````

#### Exemplo `.env`

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/aps_database
JWT_SECRET=seusegredoaqui
```

### ▶️ Rodar servidor:

```bash
npm run dev
```

A aplicação estará disponível em: `http://localhost:3000`

---

## 📌 Endpoints REST

Abaixo, os principais módulos da API:

### 🔐 Autenticação

* `POST /auth/login` → Login com geração de token JWT
* Middleware de autenticação em rotas protegidas

### 👤 Usuários

* `GET /users` → Listar todos os usuários
* `POST /users` → Criar usuário
* `PUT /users/:id` → Atualizar usuário
* `DELETE /users/:id` → Deletar usuário

### 🖊️ Autores

* `GET /authors`
* `POST /authors`
* `PUT /authors/:id`
* `DELETE /authors/:id`

### 📝 Postagens

* `GET /posts`
* `POST /posts`
* `PUT /posts/:id`
* `DELETE /posts/:id`

> Todas as rotas são documentadas automaticamente via Swagger em:
> 📄 `http://localhost:3000/api-docs`

---

## 📄 Exemplos de DTOs

```ts
// userDto.js
{
  name: "João",
  email: "joao@email.com",
  password: "123456"
}
```

```ts
// postDto.js
{
  title: "Meu primeiro post",
  content: "Conteúdo do post...",
  authorId: "65ab12cd34ef567..."
}
```

---

## 🔐 Middleware de Autenticação

As rotas protegidas usam `authMiddleware.js`, que valida o token JWT enviado no header `Authorization`.

```http
Authorization: Bearer <seu-token-jwt>
```

---

## ✅ Boas Práticas Aplicadas

* ✔️ **Arquitetura em Camadas** (Controller → Service → Repository)
* ✔️ **Uso de DTOs** para transferência segura de dados
* ✔️ **Swagger** para documentação de rotas
* ✔️ **JWT** para autenticação e proteção de rotas
* ✔️ **Repository Pattern** para desacoplar acesso a dados
* ✔️ Modularização para escalabilidade

---


---

📚 Contexto Acadêmico
Este projeto foi desenvolvido em sala de aula com o auxílio do professor e dos alunos do 7° período do curso de Bacharelado em Engenharia de Software da Faculdade UNISENAI, campus São José dos Pinhais, durante o ano de 2025.

O trabalho teve como objetivo aplicar conceitos práticos de Arquitetura de Software, organização em camadas, uso de padrões de projeto e desenvolvimento de APIs RESTful com tecnologias modernas do ecossistema Node.js.

---

## 📄 Licença

Projeto acadêmico sem fins lucrativos.
Distribuído para fins educacionais.

---
