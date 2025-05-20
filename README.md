# 📚 Blog API – Node.js, Express e SQLite

Este projeto é uma API RESTful para um sistema de blog com cadastro de usuários, autenticação JWT e postagem de mensagens.

## 🚀 Tecnologias
- Node.js
- Express.js
- SQLite com Knex.js
- JWT (Json Web Token)
- bcryptjs

---

## 📦 Como rodar o projeto

```bash
# Clone o repositório
git clone https://github.com/thobiask/blog-api.git
cd blog-api

# Instale as dependências
npm install

# Crie o banco de dados e tabelas
npm run criar-db

# Inicie o servidor
npm start
```

A API estará disponível em: [http://localhost:3000](http://localhost:3000)

---

## 🔐 Rotas da API

### POST /signup
Cadastra um novo usuário  
```json
{
  "nome": "Thobias",
  "email": "thobias@email.com",
  "senha": "123456"
}
```

### POST /login
Realiza login e retorna token  
```json
{
  "email": "thobias@email.com",
  "senha": "123456"
}
```

### POST /mensagens
Cria uma mensagem (token JWT obrigatório no header)  
Header:
```
Authorization: Bearer SEU_TOKEN_AQUI
```
Body:
```json
{
  "texto": "Minha primeira mensagem"
}
```

### GET /mensagens
Lista todas as mensagens cadastradas

---

## 🧑‍🏫 Desenvolvido por
Thobias Karpinski – Pós-graduação Inovação e Tecnologia – IFSC