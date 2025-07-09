# NLW Agents

Projeto desenvolvido durante o evento NLW da Rocketseat.

## Tecnologias e Bibliotecas Utilizadas

- **Node.js** + **TypeScript**
- [Fastify](https://www.fastify.io/) — Framework web para Node.js
- [Zod](https://zod.dev/) — Validação de esquemas e tipos
- [drizzle-orm](https://orm.drizzle.team/) — ORM para TypeScript/Node.js
- [drizzle-seed](https://github.com/arthurfiorette/drizzle-seed) — Seed para banco de dados
- [postgres](https://github.com/porsager/postgres) — Cliente PostgreSQL para Node.js
- [@fastify/cors](https://github.com/fastify/fastify-cors) — Middleware CORS

## Padrões de Projeto

- **Modularização**: Separação de rotas, conexão com banco e schemas.
- **Validação de ambiente**: Utilização de Zod para validação das variáveis de ambiente.
- **Snake_case**: Convenção de nomes no banco de dados via Drizzle ORM.

## Setup e Configuração

1. **Clone o repositório e instale as dependências:**

   ```sh
   npm install
   ```

2. **Configure o arquivo `.env`:**

   - Copie `.env.example` para `.env` e ajuste as variáveis se necessário.

3. **Suba o banco de dados com Docker:**

   ```sh
   docker-compose up -d
   ```

4. **Rode as migrações e seed do banco:**

   ```sh
   npx drizzle-kit migrates
   npm run db:seed
   ```

5. **Inicie o servidor em modo desenvolvimento:**
   ```sh
   npm run dev
   ```

## Scripts Principais

- `npm run dev` — Inicia o servidor em modo desenvolvimento
- `npm run start` — Executa o servidor em modo de produção
- `npm run db:generate` — Gera artefatos do Drizzle ORM
- `npm run db:migrate` — Executa as migrações do banco de dados
- `npm run db:seed` — Roda o seed do banco de dados

## Endpoints Disponíveis

- `GET /health` — Verifica o status da API
- `GET /rooms` — Lista todas as salas disponíveis
- `POST /rooms` — Cria uma nova sala
- `GET /rooms/:roomId/questions` — Lista as perguntas de uma sala
- `POST /rooms/:roomId/questions` — Cria uma nova pergunta em uma sala

Outros endpoints podem ser adicionados conforme a evolução do projeto.

---

Desenvolvido durante o NLW da Rocketseat 🚀
