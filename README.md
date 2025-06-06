� Teste Técnico – Desenvolvedor(a) Fullstack TypeScript

� Objetivo Geral

Criar uma aplicação fullstack utilizando TypeScript, composta por uma API RESTful e uma interface web ou mobile, que permita o cadastro e consulta de dados relacionados à data de admissão e salário bruto de funcionários.

� Tecnologias Esperadas

Backend:
Node.js com TypeScript (preferencialmente com NestJS, opcional: Express)

MongoDB
Mongoose ou TypeORM
Swagger (OpenAPI)

Jest (ou outro framework de testes)

Docker e Docker Compose

Frontend:
React ou React Native

TypeScript

Axios ou Fetch API

Material UI, Chakra UI, Tailwind ou similar

Jest + Testing Library

(Diferencial) Cypress ou Playwright para testes E2E

� Especificações Funcionais
� Backend
1. Endpoint Principal
Criar um endpoint POST que receba:

dataAdmissao (formato: YYYY-MM-DD)

salarioBruto (número positivo)

Retornar:

Dias, meses e anos decorridos desde a data de admissão

35% do salário bruto (com 2 casas decimais)

2. Validações
dataAdmissao: obrigatório, tipo Date, não pode estar no futuro

salarioBruto: obrigatório, positivo, com limite mínimo e máximo razoável

3. Persistência
Salvar dados enviados e resultados calculados no MongoDB

4. Consultas
GET /registros: lista todos os registros (com filtros e paginação)

GET /registros/:id: retorna um registro específico por ID

5. Tratamento de Erros
Padronizar erros em JSON com: status, mensagem, e timestamp

Utilizar exception filter global (NestJS) ou middleware

6. Documentação
Documentar todos os endpoints com Swagger/OpenAPI

Incluir exemplos de request/response

7. Testes
Testes unitários da lógica de cálculo

Testes de integração dos endpoints principais

8. Docker
Incluir Dockerfile e docker-compose.yml com:

Aplicação

MongoDB

� Frontend
1. Formulário de Cadastro
Campos: Data de Admissão e Salário Bruto

Validação de campos e envio para a API

Exibir:

Dias, meses e anos desde a admissão

35% do salário bruto

2. Listagem de Registros
Consumir a API de listagem e exibir os registros salvos

Implementar:

Filtros (por data ou faixa salarial)

Paginação

Visualização de detalhes (modal ou página)

� Requisitos de Interface
Design limpo e responsivo (desktop + mobile)

Utilização de componentes reutilizáveis

Organização modular por feature/domínio

� Requisitos Técnicos
Utilizar React com Hooks, Context ou Redux

Testes unitários com Testing Library

Tratamento de loading, erros e sucesso ao consumir a API

Boas práticas com Git (commits limpos e frequentes)

Código 100% TypeScript

� Diferenciais
Testes E2E com Cypress ou Playwright

Deploy do frontend (Vercel, Netlify, Expo, etc.)

Linter + Prettier configurados

✅ Critérios de Avaliação
Área	Avaliação
Código	Clareza, estrutura, modularização, boas práticas SOLID + Clean Code
Interface	Organização, responsividade, experiência do usuário (UX)
Validações	Robustez nas validações e tratamento de erros
Testes	Cobertura, organização e clareza dos testes unitários e de integração
Documentação	Swagger completo + instruções no README
Git	Histórico de commits com mensagens claras e uso de branches (se aplicável)

� Entrega
Subir o código em um repositório Git público ou privado (liberar acesso)

Incluir README com:

Instruções de instalação e execução (com e sem Docker)

Como rodar os testes
