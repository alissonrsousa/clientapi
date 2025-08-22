# 📌 API de Clientes

API REST para gerenciamento de clientes, desenvolvida em **Java 21** com **Spring Boot 3.5**.  
Permite operações **CRUD** (Create, Read, Update, Delete) sobre clientes.

---

## 🚀 Tecnologias
- Java 21  
- Spring Boot 3.5  
- Spring Web  
- Spring Data JPA  
- Banco de Dados H2
- Springdoc OpenAPI (Swagger)  

---

## 📂 Estrutura de Pastas
```
src/main/java/com/exemplo/clientes
 ├── controller   # Exposição de endpoints REST
 ├── service      # Regras de negócio
 ├── repository   # Acesso a dados (JPA)
 └── domain       # Entidades do domínio
```

---

## ⚙️ Configuração do Projeto

### Banco de Dados (application.properties)
```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
```

---

## ▶️ Executando o Projeto

### Via Maven
```bash
mvn spring-boot:run
```

A aplicação iniciará em:  
👉 `http://localhost:8080`

---

## 📖 Documentação da API (Swagger)

Após subir o projeto, acesse:  
- **Swagger UI:** [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)  
- **OpenAPI JSON:** [http://localhost:8080/v3/api-docs](http://localhost:8080/v3/api-docs)  
- **OpenAPI YAML:** [http://localhost:8080/v3/api-docs.yaml](http://localhost:8080/v3/api-docs.yaml)  

---

## 📌 Endpoints Principais

### Listar todos os clientes
```http
GET /clientes
```

### Buscar cliente por ID
```http
GET /clientes/{id}
```

### Criar novo cliente
```http
POST /clientes
Content-Type: application/json

{
  "nome": "João Silva",
  "email": "joao@email.com",
  "telefone": "11999999999"
}
```

### Atualizar cliente
```http
PUT /clientes/{id}
```

### Deletar cliente
```http
DELETE /clientes/{id}
```
---

## 📜 Licença
Este projeto é de uso livre para estudos e pode ser adaptado conforme necessário.
