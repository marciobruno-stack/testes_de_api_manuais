# 📥 Postman Collection

Nesta pasta está disponível a **Collection do Postman** contendo as requisições e testes elaborados para a validação da API **Restful-Booker**.

## 🚀 Como utilizar (Importação)
Você pode importar este arquivo diretamente no seu Postman para reproduzir e analisar os testes executados neste projeto.

1. Baixe o arquivo `Restful_Booker_API_Tests.postman_collection.json` que está aqui nesta pasta.
2. Abra o seu Postman.
3. Clique no botão **Import** (geralmente no canto superior esquerdo).
4. Arraste o arquivo `.json` ou selecione-o através do explorador de arquivos.
5. A coleção **Restful-Booker API Tests** aparecerá na sua barra lateral esquerda, pronta para execução!

## 🧪 O que está incluso nesta Collection?
- Requisições pré-configuradas (Headers, Body) para operações CRUD.
- Demonstração de testes positivos (caminho feliz).
- Demonstração de testes negativos focados em segurança (ex: tentativa de exclusão de reservas sem envio de token de autenticação, resultando em 403 Forbidden).
