# projeto.tasks

## Nome do projeto

**projeto.tasks** — Sistema de gerenciamento de tarefas.

## Descrição do projeto

O **projeto.tasks** é uma aplicação web para gerenciamento de usuários e tarefas. O sistema possui uma API desenvolvida em Java com Spring Boot, banco de dados PostgreSQL e uma interface web desenvolvida com Next.js.

A aplicação foi estruturada para permitir autenticação de usuários e gerenciamento das tarefas associadas a cada usuário.

## Tecnologias utilizadas

### Backend
- Java
- Spring Boot
- Spring Data JPA / Hibernate
- Spring Security
- JWT (JSON Web Token)
- Maven

### Frontend
- Next.js
- React
- JavaScript/TypeScript
- HTML/CSS

### Banco de dados
- PostgreSQL
- pgAdmin 4

### Versionamento
- Git
- GitHub

## Arquitetura do projeto

O fluxo principal da aplicação é:

```text
┌──────────────────────┐
│      Next.js         │
│      Frontend        │
└──────────┬───────────┘
           │ HTTP / JSON
           ▼
┌──────────────────────┐
│   Spring Boot API    │
│      Controller      │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│       Service        │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│      Repository      │
│   Spring Data JPA    │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│      PostgreSQL      │
└──────────────────────┘
```

A autenticação utiliza JWT. Após o login, o token é utilizado nas requisições protegidas através do cabeçalho:

```http
Authorization: Bearer SEU_TOKEN
```

## Estrutura principal

O projeto possui os seguintes módulos/conceitos principais:

- **Usuários** — cadastro e gerenciamento dos usuários.
- **Login** — autenticação e controle de acesso.
- **Tarefas** — criação e gerenciamento das tarefas vinculadas aos usuários.

No frontend, a comunicação com a API é organizada por serviços, incluindo:

```text
api.ts
authService.ts
usuarioService.ts
tarefaService.ts
```

## Entregas

### Entrega 01

**Descrição:** [Descreva aqui o que foi desenvolvido na Entrega 01.]

**Artefatos / screenshots:**
- [Link para o artefato da Entrega 01]
- [Link para os screenshots da Entrega 01]

### Entrega 02

**Descrição:** [Descreva aqui o que foi desenvolvido na Entrega 02.]

**Artefatos / screenshots:**
- [Link para o artefato da Entrega 02]
- [Link para os screenshots da Entrega 02]

### Entrega 03

**Descrição:** [Descreva aqui o que foi desenvolvido na Entrega 03.]

**Artefatos / screenshots:**
- [Link para o artefato da Entrega 03]
- [Link para os screenshots da Entrega 03]

> Adicione ou remova seções de acordo com a quantidade real de entregas do projeto.

## Como rodar o projeto

### Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

- Java
- Maven
- Node.js e npm
- PostgreSQL
- Git

### 1. Clonar o repositório

```bash
git clone https://github.com/jetd-ernesto/projeto.tasks.git
cd projeto.tasks
```

### 2. Configurar o banco de dados

Crie um banco PostgreSQL para o projeto e configure as credenciais utilizadas pela API.

Exemplo de configuração:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/NOME_DO_BANCO
spring.datasource.username=SEU_USUARIO
spring.datasource.password=SUA_SENHA
```

> Não coloque senhas reais ou tokens diretamente no README ou no repositório.

### 3. Executar o Backend

Entre na pasta do backend/API e execute:

```bash
./mvnw spring-boot:run
```

No Windows, caso necessário:

```bash
mvnw.cmd spring-boot:run
```

### 4. Executar o Frontend

Entre na pasta do frontend:

```bash
npm install
npm run dev
```

Depois, acesse:

```text
http://localhost:3000
```

> Ajuste os comandos e caminhos acima caso a estrutura final do repositório tenha nomes diferentes.

## Banco de dados

O sistema utiliza as principais entidades:

```text
usuario
   │
   ├─────────────── login
   │
   └─────────────── tarefas
```

A tabela `tarefas` possui relacionamento com `usuario`, permitindo associar cada tarefa ao usuário responsável.

## Equipe

| Nome completo | E-mail School |
|---|---|
| [Nome do membro 1] | [email] |
| [Nome do membro 2] | [email] |
| [Nome do membro 3] | [email] |

## Membros anteriores

Caso tenham ocorrido alterações na composição do grupo:

| Nome completo | E-mail School | Data de entrada | Data de saída |
|---|---|---|---|
| [Nome] | [email] | [DD/MM/AAAA] | [DD/MM/AAAA] |

> Caso não tenha ocorrido alteração no grupo, esta seção pode informar: **Não houve membros anteriores.**

## Repositório

Código-fonte do projeto:

https://github.com/jetd-ernesto/projeto.tasks

