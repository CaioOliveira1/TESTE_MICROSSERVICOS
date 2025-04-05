# Microsserviço de Processos

Projeto desenvolvido como parte de um desafio técnico para vaga de Analista de Sistemas Júnior.

O objetivo é disponibilizar um microsserviço para cadastro e gerenciamento de números de processos jurídicos, utilizando Spring Boot, PostgreSQL e Liquibase para versionamento do banco de dados.

---

## 🔧 Tecnologias Utilizadas

- Java 17  
- Spring Boot  
- Spring Data JPA  
- PostgreSQL  
- Liquibase  
- JUnit

---

## ▶️ Como rodar o projeto

### Pré-requisitos

- Java 17 instalado  
- PostgreSQL instalado  
- Maven instalado

### 1. Clone o repositório

```bash
git clone https://github.com/CaioOliveira1/TESTE_MICROSSERVICOS.git
```

### 2. Configure o banco de dados

No arquivo `application.yml`, altere as credenciais de acordo com sua instalação local do PostgreSQL.

```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/seu_banco
    username: seu_usuario
    password: sua_senha
```

### 3. Execute o projeto

```bash
./mvnw spring-boot:run
```

A aplicação estará disponível em:  
📍 http://localhost:8080

---

## 🔁 Estrutura do banco de dados

A estrutura do banco é criada automaticamente através do Liquibase.  
O script de versionamento está localizado em:

```
src/main/resources/db/changelog/
```

---

## 📌 Funcionalidades

- ✅ Cadastro de número de processo via POST  
- ✅ Validação de duplicidade (processos devem ser únicos)  
- ✅ Consulta de processos via GET  
- ✅ Exclusão de processo via DELETE  
- ✅ Associação de réu a um processo via PUT

---

## 📮 Endpoints disponíveis

| Método | Rota                    | Descrição                        |
|--------|-------------------------|----------------------------------|
| POST   | /processos              | Cadastrar novo processo          |
| GET    | /processos              | Listar todos os processos        |
| DELETE | /processos/{id}         | Deletar processo pelo ID         |
| PUT    | /processos/{id}/reus    | Adicionar réu a um processo      |

---

## 👨‍💻 Autor

**Caio Oliveira**  
https://github.com/CaioOliveira1

---

## 🧪 Testes

O projeto possui testes de integração utilizando JUnit para garantir o funcionamento dos endpoints.

---

## 📦 Extras

Caso deseje rodar com Docker (opcional), posso auxiliar com isso futuramente também.
