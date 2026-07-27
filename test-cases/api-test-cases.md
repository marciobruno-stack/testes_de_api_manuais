# 🧪 Casos de Teste - API (Restful-Booker)

| ID | Endpoint | Método | Descrição | Payload (Body) | Resultado Esperado | Status Code |
|:---|:---|:---|:---|:---|:---|:---|
| API-01 | `/auth` | POST | Gerar token de autenticação com sucesso | `{"username":"admin", "password":"password123"}` | Retornar um `token` válido no JSON da resposta. | `200 OK` |
| API-02 | `/auth` | POST | Tentar gerar token com senha inválida | `{"username":"admin", "password":"senhaerrada"}` | Não deve gerar o token. Deve exibir mensagem de erro. | `200 OK` (Obs: Esta API em específico retorna 200 com motivo "Bad credentials") |
| API-03 | `/booking` | GET | Listar todos os IDs de reservas | *Nenhum* | Retornar uma lista (Array) contendo objetos com `bookingid`. | `200 OK` |
| API-04 | `/booking` | POST | Criar uma nova reserva com sucesso | Dados completos (firstname, lastname, totalprice, dates) | Retornar os dados da reserva criada + `bookingid`. | `200 OK` |
| API-05 | `/booking` | POST | Tentar criar reserva sem enviar o preço (totalprice) | Payload faltando o campo numérico | API deve recusar a criação por dados incompletos. | `400 Bad Request` ou `500` (caso falhe o tratamento) |
| API-06 | `/booking/{id}`| DELETE | Tentar deletar reserva SEM estar autenticado | *Nenhum* | Operação deve ser bloqueada. Reserva não deve sumir. | `403 Forbidden` |
