# INICIANDO PROJETO FASTIFY

## instalar typescript

- npm i -D typescript
- npx tsc -init
- npm install -D @types/node

## instalar fastify

- npm i fastify

### Rodar projeto

- npx tsc src/server.ts
- node src/server.js

# Qualidade de código

### eslint

     - npm i eslint @rocketseat/eslint-config -D

- aplicar ao salvar: settings.json => "source.fixAll.eslint": true

### dotenv

para ler variaveis ambiente

### zod

- biblioteca de validação de dados
- uso para configurar variaveis ambientes: env/index.ts

# BANCO DE DADOS

## SQLITE

## SQL QUERY BUILDER

- É um construtor de querys, facilita a escrita de consultas sql e mode mudar de banco de dados sem alterar as consultas
- query builder usado: { Knex - https://knexjs.org/guide/#node-js }
- configuração : database.ts e knexfile.ts

# Cookies

     - npm i @fastify/cookie

- Formas de manter contexto entre requisições. Ou seja, identifica se é o mesmo usuário fazendo as requisições
- São enviados automaticamente nas requisições dentro de request
- o middlewares são interceptadores que podem verificar se os cookies estão sendo enviados

# Teste Automatizados

Nessa aplicação todos os testes são E2E

## Conceitos

- / conceito /: é a forma de manter a confiança na hora de fazer manutenção no código a longo prazo. Pois isso garante que todas as funcionalidades estão funcionando devidamente.
- teste unitários: testa uma unidade/função/um pedaço da aplicação, de forma totalmente isolada
- teste de integração: teste a comunicação entre duas ou mais unidades
- e2e: ponta-a-ponta - simula um usuário operando na nossa aplicação - no back-end é testar as portas de entrada da aplicação

### pirâmide de testes

- EAE : não depende de nenhum tecnologia. Apesar de serem demorados e por isso tem poucos
- integração: tem mais por ser mais rapido
- unitário: estão na base por serem mais rápidos de fazer

## framework de testes

- Vitest

  - npm i vitest -D

- requisições fake

  - supertest: ajuda a fazer requisições fake
  - npm i supertest -D

- banco de dados para teste (para testes E2E)
  criar .env.test e configurar dentro de env/index

# build e publicação

## transpilador

- tsup: https://tsup.egoist.dev/
- dentro de package => "build": "tsup src --out-dir build"

## subindo pra o git hub

- gh auth
- git init .
- git commit am
- gh repo create
