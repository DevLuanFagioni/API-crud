
# 🧩 CRUD API com Node.js, Express, MongoDB e EJS

Este projeto é uma API web simples construída com **Node.js**, **Express**, **MongoDB** (via Mongoose) e **EJS** como mecanismo de renderização. O sistema permite **criar**, **visualizar**, **editar** e **deletar** usuários.

<img width="1552" height="583" alt="tela1" src="https://github.com/user-attachments/assets/61963919-eec5-40ba-bca4-978175a66bad" />
<img width="1571" height="677" alt="tela2" src="https://github.com/user-attachments/assets/564c137c-abdf-4342-bdc5-6b000bf54196" />
<img width="1572" height="847" alt="tela3" src="https://github.com/user-attachments/assets/98c8a2d8-047e-4ef0-90b4-2f05856b2e9c" />

## 🚀 Funcionalidades

- Criar usuários
- Listar todos os usuários
- Visualizar detalhes de um usuário
- Editar informações de um usuário
- Deletar usuários
- Renderização dinâmica com EJS
- Middleware de tratamento de erro 404

---

## 🛠️ Tecnologias Utilizadas

- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)
- [EJS](https://ejs.co/)
- HTML/CSS (via pasta `public/`)

---

## 📦 Instalação

### 1. Clone o repositório

```bash
git clone [https://github.com/seu-usuario/nome-do-repo.git](https://github.com/DevLuanFagioni/API-crud.git)
cd nome-do-repo
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure a string de conexão MongoDB

Edite o valor de `dbURI` no arquivo principal:

```js
const dbURI = "mongodb+srv://<usuario>:<senha>@<cluster>.mongodb.net/nome-db";
```

---

## ▶️ Rodando o Projeto

```bash
node app.js
```

> O servidor rodará na porta `8080` (após conectar ao banco com sucesso).

---

## 📁 Estrutura de Rotas

| Rota                | Método | Descrição                                        |
|---------------------|--------|--------------------------------------------------|
| `/`                 | GET    | Redireciona para `/users`                        |
| `/users`            | GET    | Lista todos os usuários                          |
| `/user/create`      | GET    | Renderiza formulário para novo usuário           |
| `/user/create`      | POST   | Cria um novo usuário no banco                    |
| `/users/:id`        | GET    | Detalha um usuário específico                    |
| `/edit/:name/:action` | GET | Página de edição de usuário                      |
| `/edit/:id`         | POST   | Atualiza dados do usuário                        |
| `/users/:name`      | POST   | Deleta o usuário pelo nome                       |
| `/about`            | GET    | Página "Sobre"                                   |
| `*`                 | -      | Rota de erro 404                                 |

---

## 📦 Modelo `User`

O modelo `User` (MongoDB via Mongoose) está localizado em:

```js
./models/user.js
```

Certifique-se de definir o schema com os campos esperados conforme o formulário da aplicação.

---

## 📃 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
