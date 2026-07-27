# 🐛 Bug Report - Falha de Segurança em Endpoint (Exemplo)

**Título:** Endpoint DELETE `/booking/{id}` permite exclusão sem cabeçalho de autenticação.
**Endpoint:** `https://restful-booker.herokuapp.com/booking/1`
**Método HTTP:** `DELETE`
**Severidade:** Crítica
**Prioridade:** Alta

## Passos para Reproduzir:
1. Abrir o Postman.
2. Criar uma requisição `DELETE` apontando para o endpoint `/booking/1` (ou qualquer ID válido).
3. Na aba *Headers* ou *Auth*, **não** preencher nenhuma informação de autenticação (sem token/sem cookie).
4. Clicar em "Send".

## Resultado Esperado:
A API deveria validar a ausência de autenticação e retornar o Status Code **`403 Forbidden`** ou **`401 Unauthorized`**. A reserva não deveria ser deletada do banco de dados.

## Resultado Obtido (Bug):
A API retornou **`201 Created`** (ou `200 OK`) e efetivou a deleção, permitindo que qualquer usuário não autenticado apague dados do sistema.

## Evidência:
*(Adicione aqui um print do Postman mostrando a requisição feita, o status code retornado e a ausência de Auth no header)*
