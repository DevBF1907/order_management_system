# 📦 Order Management System (OMS)

API REST desenvolvida em **Java + Spring Boot** para **gerenciamento de pedidos**, simulando um sistema real utilizado por e-commerces e empresas de logística.

Este projeto foi construído com foco em **boas práticas**, **regras de negócio reais** e **padrões utilizados no mercado**, indo além de um simples CRUD.

---

## 🎯 Objetivo do Projeto

Demonstrar na prática:

* **Modelagem de domínio** baseada em regras de negócio
* Criação de **APIs REST profissionais**
* Uso correto do **Spring Boot + JPA/Hibernate**
* Separação de responsabilidades (Controller, Service, Repository)
* Validações, exceções e cálculos no back-end

Projeto ideal para **portfólio**, **entrevistas técnicas** e **avaliações práticas**.

---

## 🧠 Regras de Negócio Implementadas

* Um **pedido** inicia com status `CRIADO`
* O **total do pedido** é calculado automaticamente no back-end
* O **subtotal de cada item** é calculado com base em quantidade × preço
* Um pedido:

  * Só pode ser **pago** se estiver `CRIADO`
  * Não pode ser pago duas vezes
  * Evolui corretamente de status (`CRIADO → PAGO → ENVIADO`)

Essas regras garantem **consistência**, **segurança** e **fidelidade ao mundo real**.

---

## 🏗️ Arquitetura do Projeto

```text
src/main/java/com/brenno/oms
├── controller   # Camada de entrada (REST)
├── dto          # Objetos de transferência de dados
├── entity       # Entidades JPA
├── enums        # Enumerações (Status do Pedido)
├── exception    # Exceções e Handler global
├── repository   # Acesso ao banco de dados
├── service      # Regras de negócio
└── OrderManagementApplication.java
```

📌 **Controllers não possuem lógica de negócio**.
📌 **Services concentram as regras e validações**.

---

## 🧱 Principais Entidades

* **Cliente**
* **Produto**
* **Pedido**
* **ItemPedido**

### Status do Pedido

```text
CRIADO
PAGO
ENVIADO
CANCELADO
```

---

## 🌐 Endpoints Principais

### 📌 Pedido

| Método | Endpoint            | Descrição                    |
| ------ | ------------------- | ---------------------------- |
| POST   | /pedidos            | Criar um novo pedido         |
| POST   | /pedidos/{id}/pagar | Realizar pagamento do pedido |
| GET    | /pedidos/{id}       | Buscar pedido por ID         |

📘 Todos os endpoints estão documentados via **Swagger**.

---

## 📘 Documentação da API (Swagger)

Após subir a aplicação, acesse:

```
http://localhost:8080/swagger-ui.html
```

---

## 🛠️ Tecnologias Utilizadas

* **Java 17**
* **Spring Boot 3**
* **Spring Web**
* **Spring Data JPA**
* **Hibernate**
* **MySQL** (ou PostgreSQL)
* **Lombok**
* **Bean Validation**
* **Swagger / OpenAPI**
* **Maven**


---

## ▶️ Como Executar o Projeto

1. Clone o repositório
2. Configure o banco de dados
3. Execute a aplicação:

```bash
mvn spring-boot:run
```

4. Acesse o Swagger para testar os endpoints

---

## 🚀 Possíveis Evoluções

* Autenticação e autorização com **JWT**
* Controle de estoque automático
* Cancelamento de pedidos
* Logs e auditoria
* Dockerização
* Arquitetura Hexagonal / DDD
* Testes automatizados

---

## 👨‍💻 Autor

**Brenno**
Estudante e desenvolvedor Back-end Java
Foco em **Spring Boot**, **APIs REST** e **boas práticas de arquitetura**.

