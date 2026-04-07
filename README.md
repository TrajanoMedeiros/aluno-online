# Aluno Online API 🎓

Sistema de gestão escolar simples para o gerenciamento de registros de alunos e professores, desenvolvido como trabalho acadêmico utilizando **Spring Boot 3** e **PostgreSQL**.

## 🚀 Funcionalidades

O projeto consiste em um **CRUD** completo para as seguintes entidades:

*   **Alunos**: Cadastro, listagem, atualização de dados e remoção.
*   **Professores**: Cadastro, listagem, atualização de dados e remoção.

## 🛠️ Tecnologias Utilizadas

*   **Linguagem**: Java 21
*   **Framework**: Spring Boot 3.4.3
*   **Banco de Dados**: PostgreSQL
*   **Gerenciador de Dependências**: Maven

## ⚙️ Como Executar

### 1. Criar o Banco de Dados
No terminal, execute o comando para criar o banco que o projeto espera:
```bash
psql -U postgres -c "CREATE DATABASE \"aluno-online\";"
```

### 2. Configurar Propriedades
Verifique o arquivo `src/main/resources/application.properties` e ajuste a senha do seu PostgreSQL:
```properties
spring.datasource.password=sua_senha
```

### 3. Rodar a Aplicação
Execute o comando abaixo na raiz do projeto:
```bash
./mvnw spring-boot:run
```
O servidor iniciará na porta **8081**: `http://localhost:8081`

## 📸 Como Testar (Insomnia/Postman)

### **Rotas de Alunos**
*   `POST /aluno/create`: Criar novo aluno.
*   `GET /aluno/`: Listar todos os alunos.
*   `GET /aluno/{id}`: Buscar aluno pelo ID.
*   `PUT /aluno/update/{id}`: Atualizar dados de um aluno.
*   `DELETE /aluno/delete/{id}`: Remover um aluno.

**Exemplo de JSON para Cadastro:**
```json
{
  "name": "João da Silva",
  "email": "joao@email.com",
  "cpf": "111.222.333-44"
}
```

### **Rotas de Professores**
*   `POST /professor/create`: Criar novo professor.
*   `GET /professor/`: Listar todos os professores.
*   `GET /professor/{id}`: Buscar professor pelo ID.
*   `PUT /professor/update/{id}`: Atualizar professor.
*   `DELETE /professor/delete/{id}`: Remover professor.

**Exemplo de JSON para Cadastro:**
```json
{
  "name": "Prof. Wilson",
  "email": "wilson@email.com",
  "cpf": "999.888.777-66"
}
```

---
*Desenvolvido por Artur Medeiros para fins acadêmicos.*
