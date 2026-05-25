# 🧪 Testes de API com Postman

Este repositório contém uma coleção de testes de API desenvolvidos utilizando o Postman, com foco na validação de endpoints, regras de negócio e qualidade das respostas.

---

## 🎯 Objetivo

Praticar testes de API aplicando conceitos de Quality Assurance, garantindo que os serviços retornem dados corretos, consistentes e dentro do esperado.

---

## 🔍 Escopo dos Testes

Foram realizados testes cobrindo:

- ✔️ Validação de status code (200, 400, 404)
- ✔️ Verificação da estrutura do response body
- ✔️ Validação de dados retornados pela API
- ✔️ Testes de cenários positivos e negativos
- ✔️ Análise de tempo de resposta

---

## 🛠️ Tecnologias Utilizadas

- Postman
- JavaScript (scripts de teste)

---

## ▶️ Como Executar

1. Clone este repositório
2. Importe a collection no Postman
3. Execute as requisições individualmente ou via Collection Runner
4. Verifique os resultados na aba **Tests**

---

## 📌 Exemplos de Testes

### ✔️ Validação de Status Code

✔️ Validação de Tempo de Resposta
```javascript
pm.test("Deve retornar status 200", function () {
    pm.response.to.have.status(200);
});

✔️ Validação de Estrutura do JSON
pm.test("Tempo de resposta menor que 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
pm.test("Resposta deve conter campo 'id'", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.have.property("id");
});
