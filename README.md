# postman-api-tests
Projeto desenvolvido como prática de fundamentos de integração via API REST, com foco em troubleshooting básico e interpretação de respostas HTTP
# Postman API Tests (REST)

Repositório de prática e demonstração de testes básicos de API usando **Postman**, com foco em:
- Requisições HTTP (GET / POST)
- Análise de **status codes**
- Envio e leitura de **JSON**
- Troubleshooting básico de integrações

##  API utilizada (pública para testes)
Foi utilizada a API pública **JSONPlaceholder** para simular cenários reais de integração:
https://jsonplaceholder.typicode.com

##  Testes realizados

### 1) GET - Buscar recurso existente
- Método: `GET`
- Endpoint: `/posts/1`
- Objetivo: validar retorno de dados em JSON
- Status retornado: `200 OK`
- Resultado: retorno com JSON do recurso solicitado

### 2) GET - Buscar recurso inexistente (erro controlado)
- Método: `GET`
- Endpoint: `/posts/999999`
- Objetivo: simular cenário de “recurso não encontrado”
- Status esperado: `404 Not Found`
- Resultado: API retornou 404, indicando recurso inexistente

### 3) POST - Criar recurso
- Método: `POST`
- Endpoint: `/posts`
- Body (raw JSON):
```json
{
  "title": "Primeira criação via API",
  "body": "Estou aprendendo Postman",
  "userId": 1
}
## Aprendizados

Durante os testes, foi possível compreender:

- Diferença entre métodos GET e POST
- Interpretação de códigos de status HTTP (200, 201, 404)
- Estrutura e envio de JSON no body da requisição
- Importância da validação de endpoint e parâmetros
## 📷 Evidências dos testes

### GET - 200 OK
![GET 200](prints/get_200.png)

### GET - 404 Not Found
![GET 404](prints/get_404.png)

### POST - 201 Created
![POST 201](prints/post_201.png)
