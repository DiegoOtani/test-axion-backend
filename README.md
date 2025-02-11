# API do Projeto de teste técnico da AxionCompany

## 📌 Considerações
* Este backend foi desenvolvido como parte de um desafio técnico da empresa AxionCompany.
* O projeto é uma continuidade da API disponibilizada para o teste de desenvolvedores em https://github.com/AxionCompany/axion-test
* Projeto frontend pode ser acessado em: https://github.com/DiegoOtani/test-axion-frontend

## 🚀 Tecnologias Utilizadas

- [Strapi](https://strapi.io/)
- [Node.js](https://nodejs.org/)
- [SQLite](https://www.sqlite.org/) 

## 📦 Instalação

**Para instalar o projeto é necessário NodeJs (>=14)**

1. **Clone o repositório**  
   ```sh
   git clone https://github.com/DiegoOtani/test-axion-backend.git
   cd test-axion-backend
   ```

2. **Instale as dependências**
    ```sh
    npm install
    ```

3. **Configure as variáveis de ambiente**
   * Crie um arquivo **.env** na raíz do projeto e adicione
   ```sh
    PORT=1337
    JWT_SECRET="sua_chave_secreta"
   ```

4. **Execute o Strapi**
  * Executar a aplicação em modo de desenvolvimento
    ```sh
    npm run develop
    ```

  * Gerar a build do projeto:
    ```sh
    npm run build
    ```

5. **Usuário admin cadastrado no Strapi:**
    ```
    user: axioner@axion.company
    senha: Axioner123
    ```

## 🔗 Rotas da API

### 🛠 Autenticação

| Método | Rota                     | Descrição                 | Corpo da Requisição              |
|--------|---------------------------|---------------------------|----------------------------------|
| POST   | `/auth/local`         | Login de usuário         | `{ "identifier": "email", "password": "senha" }` |
| POST   | `/auth/local/register`| Registro de usuário      | `{ "username": "nome", "email": "email", "password": "senha" }` |

### 🍽️ Alimentos

| Método | Rota                     | Descrição                  | Requer Autenticação |
|--------|---------------------------|----------------------------|---------------------|
| GET    | `/foods`              | Lista todos os alimentos   | ✅ Sim |
| GET    | `/foods/:id`          | Retorna um alimento        | ✅ Sim |

### ✈ Lugares

| Método | Rota                     | Descrição                  | Requer Autenticação |
|--------|---------------------------|----------------------------|---------------------|
| GET    | `/places`              | Lista todos os lugares   | ✅ Sim |
| GET    | `/places/:id`          | Retorna um lugar        | ✅ Sim |

### 🙋🏻‍♂️ Pessoas

| Método | Rota                     | Descrição                  | Requer Autenticação |
|--------|---------------------------|----------------------------|---------------------|
| GET    | `/people`              | Lista todas as pessoas   | ✅ Sim |
| GET    | `/people/:id`          | Retorna uma pessoa        | ✅ Sim |
