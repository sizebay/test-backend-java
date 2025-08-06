# Teste Técnico - Desenvolvedor Back-end Pleno - Sizebay

Bem-vindo ao desafio técnico para a vaga de **Desenvolvedor Back-end** na **Sizebay**!  
Aqui você desenvolverá uma API RESTful para simular o gerenciamento de produtos e estoque de um e-commerce.

---

##  Desafio

Desenvolver uma API RESTful para gerenciar:

- Cadastro de marcas e categorias
- Cadastro de produtos com variações
- Controle de entrada e saída de estoque
- Relatórios de movimentações e saldo

Você pode usar **qualquer framework Java** (Spring Boot, Quarkus, Micronaut etc.) ou **Java puro**.

---

## Funcionalidades

### Marcas e Categorias
- CRUD completo
- Campos: `nome`, `slug`, `ativo`

### Produtos
- CRUD completo
- Campos:
  - `nome`
  - `sku`
  - `descricao`
  - `preco`
  - `marca_id`
  - `categoria_id`
  - `tamanhos_disponiveis`
  - `cores_disponiveis`

### Estoque
- Registro de entradas e saídas por SKU
- Campos:
  - `sku`
  - `quantidade`
  - `tipo` (entrada/saida)
  - `data`
- Consulta de saldo atual

---

## Tecnologias Utilizadas

- Java 17+
- Spring Boot (ou outro framework à sua escolha)
- Maven ou Gradle
- Banco de dados (PostgreSQL, MySQL ou outro)
- Swagger / OpenAPI
- Docker
- Docker Compose

---

## Como Executar Localmente com Docker

### 1. Build do projeto

Se estiver usando **Maven**:

```bash
./mvnw clean package -DskipTests
```

Ou com **Gradle**:

```bash
./gradlew clean build -x test
```

### 2. Build da imagem Docker

```bash
docker build -t sizebay-backend:latest .
```

### 3. Subir com Docker Compose

```bash
docker-compose up -d
```

### 4. Acessar a API

- Swagger: [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
- JSON e XML disponíveis via headers `Accept: application/json` ou `application/xml`

---

## Executar os Testes

Se houver testes implementados:

```bash
./mvnw test
```

ou

```bash
./gradlew test
```

---

## 🧠 Questionário Técnico

Responda às perguntas abaixo neste README (ou em um arquivo separado, ex: `RESPOSTAS.md`):

### 1. REST e Documentação
- O que caracteriza uma API RESTful bem construída?
- Quais as vantagens de usar Swagger/OpenAPI?
- Como você versionaria essa API?

### 2. Modelagem e Banco de Dados
- Diferença entre chave primária e estrangeira?
- Como você modelou produto x estoque?
- Prós e contras de usar NoSQL nesse caso?

### 3. Metodologias Ágeis
- Como garantiria entregas frequentes com qualidade?
- Qual a importância da comunicação entre times?

### 4. DevOps
- O que significa CI/CD pra você?
- Que ferramentas usaria para automação e monitoramento?

---

## Requisitos Obrigatórios

- API RESTful funcional e documentada
- Dockerfile e docker-compose funcionais
- README com instruções completas
- CRUD de marcas, categorias e produtos
- Controle de estoque (entrada e saída)

---

## Pontos Extras

- Autenticação (ex: JWT)
- Paginação e filtros
- TDD com testes unitários e integração
- Relatórios:
  - Saldo por SKU
  - Movimentação por período

---

## Submissão

- Faça um **fork deste repositório**
- Suba seu código em uma branch `main` ou `develop`
- Commitar frequentemente durante o desenvolvimento
- Inclua este README atualizado com:
  - Instruções de execução
  - Respostas ao questionário
  - Link da documentação Swagger

---

## Obrigado

Agradecemos sua dedicação e tempo. Boa sorte!  
Esperamos te ver com a gente na Sizebay! 🚀
