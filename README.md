# Transactions Api

## Sobre

Transactions Api é um projeto Node.js construído para fins de estudo. Uma API HTTP Rest é implementada com Typescript, Fastify, Knex, PostgreSQL e muito mais.

Com esta API é possível criar e listar transações. Cada transação tem um título, uma quantia em dinheiro e um tipo (crédito ou débito).

O aplicativo é totalmente testado com testes E2E feitos com Vitest e Supertest.

## Requisitos Funcionais(RF)

- O usuário deve poder criar uma conta;
- O usuário deve poder obter um extrato da sua conta;
- O usuário deve poder listar todas transações que já ocorreram;
- O usuário deve poder visualizar uma transação única;

## Regras de Negócios(RN)

- A transação pode ser do tipo crédito que somará ao valor total, ou débito que será subtraído;
- Deve ser possível identificar o usuário entre as requisições;
- O usuário só pode visualizar transações que ele criou;

## Rotas

|HTTP Method|Route|Description|Request body|
|:----|:----|:----|:----|
|GET|/transactions|Returns a list of the transactions|N/A|
|POST|/transactions|Creates a new transaction|title            amount            type (credit or debit)|
|GET|/transactions/:id|Returns a transaction with the given id|N/A|
|GET|/summary|Returns a summary of the transactions|N/A|

## Tecnologias

Algumas tecnologias utilizadas para construção da aplicação.

- Node.js
- Datilografado
- Fastificar
- Knex
- PostgreSQL
- SQLite
-Zod
- TSup
- Vitest
- Superteste

## Rodar o servidor

- Para rodar o servidor localmente
  1. Criar arquivo `.env` baseado em `.env.example`
  2. Execute `npm i` para instalar as dependências
  3. Execute `npm run knex -- migration:latest` para executar as migrações
  4. Execute o servidor de desenvolvimento com `npm run dev`

### Executando testes E2E

- Criar arquivo `.env.test` baseado em `.env.test.example`
- Execute `npm test`
