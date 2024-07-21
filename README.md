# ToDo List API

## Sumário
1. [Introdução](#introdução)
2. [Funcionalidades](#funcionalidades)
3. [Endpoints](#endpoints)
4. [Tecnologias Utilizadas](#tecnologias-utilizadas)
5. [Pré-requisitos](#pré-requisitos)
6. [Instalação e Execução](#instalação-e-execução)
7. [Contato](#contato)
8. [Autor](#autor)

## Introdução
A ToDo List API é uma aplicação backend desenvolvida em Java para gerenciar listas de tarefas. Ela permite o cadastro de usuários, autenticação, criação, atualização e listagem de tarefas.

## Funcionalidades
- **Cadastro de um novo usuário:** Permite registrar um novo usuário no sistema.
- **Sistema básico de autenticação:** Autenticação de usuários para garantir que apenas usuários autorizados possam acessar e modificar seus dados.
- **Cadastro de uma nova task:** Permite que um usuário registre uma nova tarefa.
- **Atualização de uma task:** Permite que um usuário atualize uma tarefa existente.
- **Listagem das tasks de um usuário:** Exibe todas as tarefas cadastradas pelo usuário.

## Endpoints

### Cadastro de usuários
- Rota: `POST /users/`
- Request body (JSON):
  ```json
  {
    "user": "user",
    "username": "username",
    "password": "password"
  }
  ```
- Response body (JSON):
  ```json
    {
      "id": "id",
      "username": "username",
      "name": "name",
      "password": "password",
      "createdAt": "createdAt"
    }
  ```
### Cadastro de uma nova task
- Rota: `POST /tasks/`
- Request body (JSON):
  ```json
    {
      "description": "description",
      "title": "title",
      "priority": "priority",
      "startAt": "startAt",
      "endAt": "endAt"
    }
  ```
- O usuário precisa se autenticar com Basic Auth.
- Response body (JSON):
  ```json
    {
      "description": "description",
      "title": "title",
      "priority": "priority",
      "startAt": "startAt",
      "endAt": "endAt",
      "userId": "userId",
      "createdAt": "createdAt"
    }
  ```
### Atualização de uma task
- Rota: `PUT /tasks/`
- Request body (JSON):
  ```json
    {
      "description": "description",
      "title": "title",
      "priority": "priority",
      "startAt": "startAt",
      "endAt": "endAt"
    }
  ```
- O usuário precisa se autenticar com Basic Auth.
- Response body (JSON):
  ```json
    {
      "description": "description",
      "title": "title",
      "priority": "priority",
      "startAt": "startAt",
      "endAt": "endAt",
      "userId": "userId",
      "createdAt": "createdAt"
    }
  ```
### Listagem das task de um usuário
- Rota: `GET /tasks/`
- O usuário precisa se autenticar com Basic Auth.
- Response body (JSON):
  ```json
    [
      {
        "description": "description",
        "title": "title",
        "priority": "priority",
        "startAt": "startAt",
        "endAt": "endAt",
        "userId": "userId",
        "createdAt": "createdAt"
      }
    ]
  ```

## Tecnologias Utilizadas
- **Java 17:** Linguagem de programação utilizada.
- **Maven:** Ferramenta de gerenciamento de dependências e construção do projeto.
- **Spring Boot:** Framework para criação de aplicações Java.
- **Spring Data JPA:** Framework para acesso a dados.
- **H2 Database Engine:** Banco de dados em memória utilizado para desenvolvimento e testes.

## Pré-requisitos
- **Java 17:** [Instalar Java 17](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- **Maven:** [Instalar Maven](https://maven.apache.org/install.html)

## Instalação e Execução

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/todo-list-api.git
    ```

2. Navegue até o diretório do projeto:
    ```bash
      cd todo-list-api
    ```

3. Compile e execute o projeto com o Maven:
    ```bash
      mvn spring-boot:run
    ```

## Contato
Para dúvidas ou sugestões, entre em contato através de:

- [Email](mailto:josevictornascimento2016@gmail.com)
- [Linkedin](https://www.linkedin.com/in/jos%C3%A9-victor-nascimento-7983b2230/)

## Autor

Feito com amor por [@josevictorn](https://github.com/josevictorn)