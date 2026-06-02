  PetShop API

  Apresentação do Projeto

 Nome do Projeto

**PetShop API**

 Objetivo do Sistema

Desenvolver uma API REST para gerenciamento de um PetShop, permitindo o controle de clientes, animais, produtos e serviços oferecidos pela empresa.

 Funcionalidades Disponíveis

* Cadastro de clientes;
* Cadastro de pets;
* Cadastro de produtos;
* Cadastro de serviços;
* Consulta de registros;
* Atualização de informações;
* Exclusão de registros;
* Relacionamento entre clientes e seus pets.



 Tecnologias Utilizadas

O projeto foi desenvolvido utilizando as seguintes tecnologias:

* Java 17
* Spring Boot
* Spring Data JPA
* Spring Web
* MySQL
* Maven
* Hibernate
* Lombok
* Postman (testes da API)
* Git e GitHub



#  Estrutura do Projeto

A aplicação segue a arquitetura em camadas:

```text
src/main/java
│
├── controller
│   ├── ClienteController.java
│   ├── PetController.java
│   └── ProdutoController.java
│
├── service
│   ├── ClienteService.java
│   ├── PetService.java
│   └── ProdutoService.java
│
├── repository
│   ├── ClienteRepository.java
│   ├── PetRepository.java
│   └── ProdutoRepository.java
│
├── entity
│   ├── Cliente.java
│   ├── Pet.java
│   └── Produto.java
│
└── config
```

 Descrição das Camadas

| Camada     | Responsabilidade           |
| ---------- | -------------------------- |
| Controller | Recebe as requisições HTTP |
| Service    | Regras de negócio          |
| Repository | Acesso ao banco de dados   |
| Entity     | Representação das tabelas  |
| Config     | Configurações do sistema   |



 Banco de Dados

 Nome do Banco

```sql
petshop_db
```

 Principais Tabelas

* cliente
* pet
* produto
* servico

 Relacionamentos

```text
CLIENTE
│
└───< PET

PET
│
└───< SERVICO
```

 DER (Exemplo)

```text
Cliente
--------
id
nome
telefone
email

Pet
--------
id
nome
idade
raca
cliente_id

Produto
--------
id
nome
preco
estoque

Servico
--------
id
descricao
valor
pet_id
```

*Inserir imagem do DER aqui caso disponível.*



 Como Executar o Projeto

 1. Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/petshop-api.git
```

 2. Abrir o Projeto

Importe o projeto em sua IDE favorita:

* IntelliJ IDEA
* Eclipse
* VS Code



 3. Criar o Banco de Dados

```sql
CREATE DATABASE petshop_db;
```



 4. Configurar o application.properties

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/petshop_db
spring.datasource.username=root
spring.datasource.password=senha

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```



 5. Executar a Aplicação

Via Maven:

```bash
mvn spring-boot:run
```

Ou executar a classe:

```java
PetshopApplication.java
```

A aplicação estará disponível em:

```text
http://localhost:8080
```



 🔗 Endpoints da API

 Clientes

| Método | URL            | Descrição             |
| ------ | -------------- | --------------------- |
| GET    | /clientes      | Listar clientes       |
| GET    | /clientes/{id} | Buscar cliente por ID |
| POST   | /clientes      | Cadastrar cliente     |
| PUT    | /clientes/{id} | Atualizar cliente     |
| DELETE | /clientes/{id} | Remover cliente       |



 Pets

| Método | URL        | Descrição         |
| ------ | ---------- | ----------------- |
| GET    | /pets      | Listar pets       |
| GET    | /pets/{id} | Buscar pet por ID |
| POST   | /pets      | Cadastrar pet     |
| PUT    | /pets/{id} | Atualizar pet     |
| DELETE | /pets/{id} | Remover pet       |



 Produtos

| Método | URL            | Descrição             |
| ------ | -------------- | --------------------- |
| GET    | /produtos      | Listar produtos       |
| GET    | /produtos/{id} | Buscar produto por ID |
| POST   | /produtos      | Cadastrar produto     |
| PUT    | /produtos/{id} | Atualizar produto     |
| DELETE | /produtos/{id} | Remover produto       |



 Funcionalidades Implementadas

* Cadastro de clientes;
* Consulta de clientes;
* Atualização de clientes;
* Exclusão de clientes;
* Cadastro de pets;
* Consulta de pets;
* Atualização de pets;
* Exclusão de pets;
* Cadastro de produtos;
* Controle de estoque;
* Relacionamento entre clientes e pets;
* Persistência de dados com MySQL;
* API REST completa.



 Desenvolvedor

**Nome Completo:** Lucca Moreira Ferreira



 Licença

Este projeto foi desenvolvido para fins acadêmicos e educacionais.
