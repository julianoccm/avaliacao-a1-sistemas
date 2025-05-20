# Avaliação A1 - Sistemas - UniCuritiba
Professor: Diego Palma

RA: 172412391

## Escopo:
Imagine que estamos desenvolvendo um sistema de aluguel de carros. Você
precisa criar um endpoint REST para cadastrar um novo cliente. O recurso deve
estar disponível em /clientes, e a requisição deve conter um JSON com os
dados: nome, CPF e telefone. Com base nisso, implemente o código do controller
no Spring Boot com o método mais apropriado (Deixe o repositório público e
adicione o usuário palma1607, com colaborador).

## Acesso banco:
URL: http://localhost:8080/h2-console/login.do?jsessionid=04af13c695a7e82c818db72117685a1d

JDBC URL: jdbc:h2:mem:testdb

Usuario: sa

Senha: senha

## Endpoints:

### **Salvar clientes:**

`POST http://localhost:8080/clientes`

Body de exemplo:
```
{

    "nome": "Juliano",
    "cpf": "123.367.279-78",
    "telefone": "41999311991"
}
```

Chamada CURL:
```
curl --location --request POST 'http://localhost:8080/clientes' \
--header 'Content-Type: application/json' \
--data '{

    "nome": "Juliano",
    "cpf": "123.367.279-78",
    "telefone": "41999311991"
}'
```

### **Pegar todos os clientes:**

`GET http://localhost:8080/clientes`

Chamada CURL:
```
curl --location 'http://localhost:8080/clientes'
```

### **Pegar cliente por Id:**

`GET http://localhost:8080/clientes/{id}`

Chamada CURL:
```
curl --location 'http://localhost:8080/clientes/1'
```
