# 📝 Plano de Testes de API - Restful-Booker

## 1. Introdução
Este plano de testes cobre a validação da API **Restful-Booker** (https://restful-booker.herokuapp.com/), um sistema base para testes de gerenciamento de reservas de hotel. O foco é garantir que as operações de criação (POST), leitura (GET), atualização (PUT) e exclusão (DELETE) estejam funcionando conforme os padrões REST.

## 2. Escopo
* **In-Scope (O que será testado):**
  - Endpoint de Autenticação (`/auth`)
  - Endpoints de Reservas (`/booking`)
  - Fluxos de validação de dados (Payloads em JSON).
  - Testes de segurança básicos (tentar deletar ou atualizar sem autenticação).

* **Out-of-Scope (O que não será testado):**
  - Testes de Carga/Performance.
  - Testes de Interface Gráfica (Frontend).

## 3. Estratégia de Testes
* **Testes Positivos:** Validar se a API responde com status 200/201 ao receber dados válidos.
* **Testes Negativos:** Enviar dados incompletos (faltando campos obrigatórios), tipos de dados incorretos e tokens inválidos para garantir que a API retorna erros coerentes (ex: 400 Bad Request ou 403 Forbidden).

## 4. Critérios de Sucesso
- 100% dos Casos de Teste planejados devem ser executados no Postman.
- Todo e qualquer status code HTTP 500 (Internal Server Error) deve ser reportado como Bug Crítico.
