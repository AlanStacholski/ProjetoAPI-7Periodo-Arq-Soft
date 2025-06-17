````markdown
# 📘 ProjetoAPSarqSoftware

**API RESTful** construída com **Node.js**, **Express** e **MongoDB**, aplicando princípios sólidos de Arquitetura de Software.  
O sistema simula um backend robusto e escalável para gerenciamento de **usuários**, **autores** e **postagens**.

---

## 🎓 Objetivo Acadêmico

Projeto realizado como parte da disciplina de **Arquitetura de Software**, com foco na aplicação prática dos seguintes conceitos:

- 🧱 Arquitetura em múltiplas camadas
- 🧠 Princípios SOLID
- ♻️ Inversão de dependência (`services` → `repositories`)
- 🧩 Separação de responsabilidades
- ⚙️ Utilização de Middlewares, DTOs e Swagger

---

## 🚀 Tecnologias Utilizadas

| 🧰 Tecnologia   | 📝 Finalidade                            |
|----------------|------------------------------------------|
| **Node.js**    | Ambiente de execução JavaScript          |
| **Express**    | Framework web minimalista                |
| **MongoDB**    | Banco de dados NoSQL                     |
| **Mongoose**   | ODM para modelagem dos dados             |
| **Swagger**    | Documentação interativa da API           |
| **Dotenv**     | Variáveis de ambiente                    |
| **Nodemon**    | Hot reload no ambiente de desenvolvimento|

---

## 🗂️ Estrutura de Pastas

```bash
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
├── app.js                     # Configuração principal do Express
├── server.js                  # Ponto de entrada do servidor
├── package.json
└── README.md
````

---

## 📦 Instalação e Execução

### ✅ Pré-requisitos

* [Node.js](https://nodejs.org/)
* MongoDB (local ou via MongoDB Atlas)
* Postman ou Insomnia (para testes)

### 🛠️ Passos para rodar o projeto

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/ProjetoAPSarqSoftware.git
cd ProjetoAPSarqSoftware

# Instale as dependências
npm install

# Crie o arquivo .env e adicione suas variáveis
touch .env
```

#### 🔐 Exemplo `.env`

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/aps_database
JWT_SECRET=seusegredoaqui
```

### ▶️ Rodar servidor em modo desenvolvimento

```bash
npm run dev
```

Acesse: [http://localhost:3000](http://localhost:3000)

---

## 🔗 Endpoints REST

### 🔐 Autenticação

* `POST /auth/login` → Login e geração de token JWT
* Middleware para rotas protegidas

### 👤 Usuários

* `GET /users` → Listar todos os usuários
* `POST /users` → Criar usuário
* `PUT /users/:id` → Atualizar usuário
* `DELETE /users/:id` → Remover usuário

### ✍️ Autores

* `GET /authors`
* `POST /authors`
* `PUT /authors/:id`
* `DELETE /authors/:id`

### 📝 Postagens

* `GET /posts`
* `POST /posts`
* `PUT /posts/:id`
* `DELETE /posts/:id`

📑 **Documentação Swagger disponível em:**
[http://localhost:3000/api-docs](http://localhost:3000/api-docs)

---

## 🧾 Exemplos de DTOs

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

## 🔒 Middleware de Autenticação

As rotas protegidas utilizam o middleware `authMiddleware.js`, que valida o token JWT via header:

```http
Authorization: Bearer <seu-token-jwt>
```

---

## ✅ Boas Práticas Aplicadas

* ✔️ Arquitetura em Camadas (Controller → Service → Repository)
* ✔️ Uso de DTOs para validação e transporte de dados
* ✔️ Swagger para documentação de rotas
* ✔️ JWT para autenticação segura
* ✔️ Repository Pattern
* ✔️ Separação clara de responsabilidades

---

## 📚 Contexto Acadêmico

Projeto acadêmico desenvolvido em **2025** pelos alunos do **7º período de Bacharelado em Engenharia de Software** da **Faculdade UNISENAI – São José dos Pinhais**, com o apoio do professor em sala de aula.

O objetivo foi a aplicação prática dos conceitos de Arquitetura de Software por meio do desenvolvimento de uma **API RESTful modularizada e escalável**.

---

## 📄 Licença

Projeto de uso **exclusivamente educacional**, sem fins lucrativos.
Distribuído sob os termos da licença acadêmica.

---
