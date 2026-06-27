# 📅 Sistema de Agendamento

Um sistema simples de agendamento desenvolvido com **Java** e **Spring Boot**, permitindo o cadastro, consulta, atualização e remoção de horários agendados.

Este projeto foi criado com foco em aprendizado de desenvolvimento de APIs REST utilizando Spring Boot.

---

## 🚀 Funcionalidades

- ✅ Criar um agendamento
- ✅ Listar todos os agendamentos
- ✅ Buscar agendamento pela a data
- ✅ Atualizar um agendamento
- ✅ Remover um agendamento

---

## 🛠️ Tecnologias

- Java 22
- Spring Boot
- Spring Web
- Spring Data JPA
- Hibernate
- Banco de dados H2
- Maven

---

## 📁 Estrutura do Projeto

```
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── javadev
│   │   │           └── agendador_horarios
│   │   │               ├── controller
│   │   │               │   └── AgendamentoController.java
│   │   │               ├── infrastructure
│   │   │               │   ├── entity
│   │   │               │   │   └── Agendamento.java
│   │   │               │   └── repository
│   │   │               │       └── AgendamentoRepository.java
│   │   │               ├── services
│   │   │               └── AgendadorHorariosApplication.java
│   │   └── resources
│   │       ├── static
│   │       ├── templates
│   │       └── application.properties
│   └── test
```

---

## 📌 Modelo da Entidade

```java
public class Agendamento {

    private Long id;
    private String servico;
    private String profissional;
    private LocalDateTime dataHoraAgendamento;
    private String cliente;
    private String telefoneCliente;
    private LocalDateTime dataInsercao = LocalDateTime.now();

}
```

---

## 📡 Endpoints da API

### Criar Agendamento

```
POST /agendamentos
```

Exemplo:

```json
{
    "servico" : "Cabelo",
    "profissional": "Barbeiro",
    "dataHoraAgendamento" : "2026-06-20T18:41",
    "cliente" : "Caue",
    "telefoneCliente": "85940028922"
}
```

---

### Listar Agendamentos

```
GET /agendamentos
```

---

### Buscar por ID

```
GET /agendamentos/{data}
```

---

### Atualizar

```
PUT /agendamentos/{cliente}
```

---

### Excluir

```
DELETE /agendamentos/{cliente}
```

---

## ▶️ Como executar

### 1 - Clone o projeto

```bash
git clone https://github.com/w-Caue/controle-agendamentos.git
```

### 2 - Entre na pasta

```bash
cd controle-agendamentos
```

### 3 - Execute

```bash
./mvnw spring-boot:run
```

ou

```bash
mvn spring-boot:run
```

A aplicação ficará disponível em:

```
http://localhost:8080
```

---

## 💾 Banco de Dados

O projeto utiliza o banco em memória **H2**.

Console:

```
http://localhost:8080/h2-console
```

Configuração padrão:

```
JDBC URL:
jdbc:h2:mem:agendamento

User:
sa

Password:
```

---

## 📷 Exemplo de resposta

```json
[
    {
        "id": 1,
        "servico": "Cabelo",
        "profissional": "Barbeiro",
        "dataHoraAgendamento" : "2026-06-20T18:41",
        "cliente" : "Caue",
        "telefoneCliente": "85940028922"
        "dataInsercao": "2026-06-20"
    }
]
```

---

## 📚 Conceitos praticados

- API REST
- Arquitetura em camadas
- CRUD
- Spring Boot
- Spring Data JPA
- Injeção de Dependência
- Persistência de dados
- Boas práticas de organização de projeto

---

## 🔮 Melhorias futuras

- Login de usuários
- Validação de conflitos de horário
- Paginação
- Filtro por data
- Busca por cliente
- Documentação com Swagger/OpenAPI
- Banco PostgreSQL
- Docker

---

## 👨‍💻 Autor

Desenvolvido por **Cauê Sousa**

LinkedIn:
https://linkedin.com/in/cauesousadev/

GitHub:
https://github.com/w-Caue
