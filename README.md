# api-entregas-algalog

Api desenvolvida no curso Mergulho Spring Rest da Algaworks utilizando o [Ecossistema Spring](https://spring.io/) em conjunto com [Jakarta Persistence JPA](https://jakarta.ee/specifications/persistence/), [Jakarta Bean Validation](https://jakarta.ee/specifications/bean-validation/), [ModelMapper](http://modelmapper.org/), [Lombok](https://projectlombok.org/) e [Flyway](https://flywaydb.org/).

Recursos da API:

1 - Clientes;<br>
2 - Entregas;<br>
3 - Ocorrências.<br>

## Endpoints

### Clientes

- Listar os clientes (GET localhost:8080/clientes);
- Obter um cliente (GET localhost:8080/clientes/{IdCliente});
- Adicionar um cliente (POST localhost:8080/clientes);<br>
  Exemplo de corpo:
  ```JSON
  {
      "nome": "Luis José",
      "email": "gustavo@algaworks.com",
      "telefone": "34 98888-7777"
  }
  ```
- Atualizar um cliente (PUT localhost:8080/clientes/{IdCliente});<br>
  Exemplo de corpo:
  ```JSON
  {
      "nome": "Fernando Silva",
      "email": "fernando@algaworks.com",
      "telefone": "34 98888-7777"
  }
  ```
- Excluir um cliente (DELETE localhost:8080/clientes/{IdCliente}).

### Entregas

- Listar as entregas (GET localhost:8080/entregas);
- Obter uma entrega (GET localhost:8080/entregas/{IdEntrega});
- Solicitar uma entrega (POST localhost:8080/entregas);<br>
  Exemplo de corpo:
  ```JSON
  {
  "cliente":{
  	"id": 1
  },
  "destinatario":{
  	"nome": "Joaquim da Silva",
  	"logradouro": "Rua das goiabas",
  	"numero": "100",
  	"bairro": "Centro",
  	"complemento": "AP 200"
  },
      "taxa": 100.50
  }
  ```
- Finalizar uma entrega (PUT localhost:8080/entregas/IdEntrega/finalizacao).

### Ocorrências

- Listar Ocorrências (GET localhost:8080/entregas/IdEntrega/ocorrencias);
- Registrar uma Ocorrência (POST localhost:8080/entregas/IdEntrega/ocorrencias).<br>
  Exemplo de corpo:
  ```JSON
  {
    "descricao": "Tentativa sem sucesso (não estava em casa)"
  }
  ```
