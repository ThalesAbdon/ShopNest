# Desafio Full Backend com NestJS

Você foi contratado para desenvolver um sistema de gestão de pedidos para um e-commerce de uma grande empresa. Esse sistema precisa ser robusto, seguro e escalável.

## Módulos da Aplicação

- **Autenticação e Usuários** (com JWT e refresh token)
- **Produtos** (CRUD com validação)
- **Pedidos** (checkout, pagamento simulado, atualização de status)
- **Filas de Processamento** (confirmação de pedidos assíncrona)
- **Cache** para otimizar performance
- **Logs e Monitoramento**

---

## Requisitos Técnicos

### 1. Autenticação e Segurança
- Criar sistema de login e cadastro usando **Passport.js e JWT**
- Implementar **refresh token** para reautenticação
- Middleware de proteção de rotas
- Restringir ações com **Guards** (ex: só admins podem deletar produtos)
- Proteção contra **CSRF, XSS, SQL Injection**

### 2. CRUD de Produtos
- Criar **endpoints RESTful** para adicionar, editar, excluir e listar produtos
- Implementar **validação de dados** com `class-validator`
- Paginação e **filtros avançados** (ex: buscar por preço, categoria)
- **Cache em Redis** para otimizar busca de produtos

### 3. Pedidos e Pagamentos
- Criar API para **checkout e criação de pedidos**
- Implementar fluxo de **pagamento simulado**
- Atualizar **status do pedido** (PENDENTE, PAGO, ENVIADO)
- Registrar **logs das ações**

### 4. Processamento Assíncrono (Mensageria)
- Após a confirmação do pedido, enviar mensagem para um **worker (Microserviço NestJS)**
- O worker processa o pedido e simula envio do **email de confirmação**
- Usar **Redis Pub/Sub, RabbitMQ ou Kafka** para comunicação assíncrona

### 5. Testes e Qualidade
- Escrever **testes unitários e e2e** com Jest e Supertest
- Implementar **linting** (ESLint, Prettier)
- Adicionar **logs detalhados** com Winston ou Pino

### 6. DevOps e Deploy
- Criar um **Dockerfile** e usar **Docker Compose**
- Implementar **CI/CD** (ex: GitHub Actions ou GitLab CI)
- **Monitoramento** com Prometheus e Grafana
- **Deploy** na AWS (ECS, Lambda) ou DigitalOcean

---

## Bônus (Desafios Extras)

- Implementar **GraphQL** como alternativa ao REST
- Criar **WebSockets** para notificar o usuário sobre status do pedido
- Criar um **Sistema de Permissões Avançado** baseado em roles
- Adicionar suporte a **gRPC** entre serviços

---

## Como Entregar?

1. Criar um **repositório no GitHub/GitLab**
2. Adicionar um **README** explicando como rodar a aplicação
3. Implementar **testes automatizados**
4. Usar **commits organizados** seguindo boas práticas
