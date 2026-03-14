# 📸 Instalike - Imersão Backend Alura

Bem-vindo ao **Instalike**, uma API desenvolvida durante a **Imersão Backend da Alura**. Este projeto simula o ecossistema de uma rede social, focando na construção de rotas, manipulação de arquivos e integração com banco de dados e Inteligência Artificial.

---

## 🛠️ Tecnologias e Ferramentas

O projeto foi construído utilizando as seguintes tecnologias:

* **Node.js**: Ambiente de execução para o JavaScript no servidor.
* **Express**: Framework web para criação de rotas e middlewares.
* **MongoDB Atlas**: Banco de dados NoSQL na nuvem para persistência dos posts.
* **Google Gemini API**: Integração com IA para geração automática de textos alternativos (Alt-text).
* **Multer**: Middleware para gerenciar o upload de imagens.
* **Postman/Insomnia**: Ferramentas para testes dos endpoints da API.

---

## 🚀 Funcionalidades

- [x] **Listar Posts:** Retorna todos os posts armazenados no banco de dados.
- [x] **Criar Post:** Permite o envio de dados textuais para o MongoDB.
- [x] **Upload de Imagem:** Processa e armazena imagens localmente na pasta `uploads/`.
- [x] **Integração com IA:** Gera descrições automáticas para as imagens utilizando o modelo Gemini da Google.

---

## 🏁 Como Rodar o Projeto

1. **Clone este repositório:**
   ```bash
   git clone [https://github.com/tamersonbonfa/instalike-backend-alura.git](https://github.com/tamersonbonfa/instalike-backend-alura.git)
   ```

   ```bash
   cd instalike-backend-alura
   ```


2. **Instale as dependências:**

   ```bash
   npm install
   ```


3. **Configure as Variáveis de Ambiente:**

   ```bash
   STRING_CONEXAO=mongodb+srv://<usuario>:<senha>@cluster.mongodb.net/sua-db
   ```

   ```bash
   GEMINI_API_KEY=sua_chave_da_google_gemini_aqui
   ```


4. **Inicie o servidor:**

   ```bash
   npm run dev
   ```

   Acesse a API em: http://localhost:3000

## 📍 Endpoints da API
| Método | Rota | Descrição |
| :--- | :--- | :--- |
| **GET** | **/posts** | Lista todos os posts cadastrados. |
| **POST** | **/posts** | Cria um novo post básico (sem imagem). |
| **POST** | **/upload** | Faz o upload de uma imagem e cria um registro. |
| **PUT** | **/upload/:id** | Atualiza o post com a descrição gerada pela IA. |

## 📁 Estrutura de Pastas

   ```bash
   ├── src/
   │   ├── config/      # Conexão com o banco de dados
   │   ├── controllers/ # Lógica de negócio e respostas das rotas
   │   ├── models/      # Consultas ao banco de dados (MongoDB)
   │   ├── routes/      # Definição dos caminhos (endpoints)
   │   └── services/    # Integrações externas (Google Gemini)
   ├── uploads/         # Repositório das fotos enviadas
   ├── server.js        # Arquivo principal de inicialização
   └── .gitignore       # Arquivos ignorados pelo Git
   ```
   Projeto desenvolvido com foco em aprendizado de arquitetura backend e integração de serviços durante a Imersão Alura. 🚀