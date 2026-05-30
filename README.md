# Caderno Temático: Desenvolvimento de APIs Performáticas com Spring Boot

## Sobre

Este projeto foi desenvolvido como parte do desafio da DIO utilizando o NotebookLM como ferramenta de aprendizagem ativa e organização do conhecimento.

O tema escolhido foi **Desenvolvimento de APIs Performáticas com Spring Boot**, uma das competências mais valorizadas no desenvolvimento backend moderno. O objetivo foi reunir materiais de referência, explorar conceitos fundamentais e avançados por meio de interações com IA e consolidar o aprendizado em um guia de estudos reutilizável.

---

# Objetivos de Estudo

Ao desenvolver este caderno temático, busquei:

- Compreender a arquitetura de aplicações REST com Spring Boot.
- Aprender técnicas para aumentar a performance de APIs.
- Estudar estratégias de cache e otimização de consultas.
- Entender boas práticas para tratamento de exceções e observabilidade.
- Conhecer mecanismos de escalabilidade e resiliência.
- Criar um material de consulta para futuros projetos backend.

---

# Curadoria de Fontes

As seguintes fontes foram selecionadas e importadas para o NotebookLM:

## 1. Spring Boot Official Documentation

**Link:**  
https://docs.spring.io/spring-boot/docs/current/reference/html/

**Conteúdo estudado:**

- Auto Configuration
- Spring MVC
- Spring Data JPA
- Actuator
- Caching

---

## 2. Spring Framework Documentation

**Link:**  
https://docs.spring.io/spring-framework/reference/

**Conteúdo estudado:**

- IoC Container
- Dependency Injection
- Web MVC
- Transaction Management

---

## 3. Baeldung - Spring Performance

**Link:**  
https://www.baeldung.com/

**Conteúdo estudado:**

- Cache com Spring
- Otimização JPA
- Performance em APIs REST
- Monitoramento

---

## 4. Hibernate ORM Documentation

**Link:**  
https://hibernate.org/orm/documentation/

**Conteúdo estudado:**

- Lazy Loading
- Fetch Strategies
- N+1 Problem
- Query Optimization

---

## 5. Spring Boot Actuator Documentation

**Link:**  
https://docs.spring.io/spring-boot/docs/current/reference/html/actuator.html

**Conteúdo estudado:**

- Health Checks
- Metrics
- Monitoring
- Observability

---

# Engenharia de Prompts e "Cicatrizes"

Durante os estudos, diversos prompts foram utilizados para extrair informações do NotebookLM.

## Prompt 1 - Fundamentos

**Pergunta:**

> Explique como funciona o ciclo de vida de uma requisição HTTP em uma API Spring Boot.

**Resultado:**

- Boa explicação do fluxo Controller → Service → Repository.
- Introdução adequada aos componentes do framework.

**Aprendizado:**

Prompts conceituais ajudam a construir uma base sólida antes de avançar para otimizações.

---

## Prompt 2 - Performance

**Pergunta:**

> Quais são os principais gargalos de performance em APIs Spring Boot e como mitigá-los?

**Resultado:**

- Identificação de problemas relacionados ao banco de dados.
- Destaque para cache e paginação.

**Aprendizado:**

Solicitar causas e soluções produz respostas mais completas.

---

## Prompt 3 - JPA

**Pergunta:**

> Explique o problema N+1 Query e apresente exemplos de solução utilizando Spring Data JPA.

**Resultado:**

- Excelente detalhamento técnico.
- Exemplos envolvendo JOIN FETCH e EntityGraph.

**Aprendizado:**

Prompts específicos produzem respostas mais úteis para aplicação prática.

---

## Prompt 4 - Observabilidade

**Pergunta:**

> Como utilizar Spring Boot Actuator para monitorar APIs em produção?

**Resultado:**

- Explicação dos endpoints de monitoramento.
- Demonstração das métricas disponíveis.

**Aprendizado:**

Solicitar cenários reais melhora a contextualização.

---

## Prompt 5 - Escalabilidade

**Pergunta:**

> Crie um checklist para construção de APIs REST escaláveis utilizando Spring Boot.

**Resultado:**

- Lista estruturada de boas práticas.
- Fácil utilização como referência futura.

**Aprendizado:**

Prompts orientados a entregáveis geram materiais mais reaproveitáveis.

---

# Dificuldades Encontradas (Cicatrizes)

## Problema 1

Respostas muito superficiais sobre performance.

### Solução

Adicionar contexto técnico ao prompt.

**Exemplo:**

Ao invés de:

> Como melhorar a performance de uma API?

Utilizar:

> Como melhorar a performance de uma API Spring Boot com banco PostgreSQL que processa mais de 10 mil requisições por minuto?

---

## Problema 2

Falta de exemplos práticos.

### Solução

Solicitar explicitamente:

> Forneça exemplos de código e explique as vantagens e desvantagens de cada abordagem.

---

## Problema 3

Excesso de conteúdo teórico.

### Solução

Solicitar resumos executivos e listas de boas práticas.

---

# Miniguia de Estudos

## 1. Arquitetura Básica de APIs Spring Boot

Uma aplicação Spring Boot normalmente é organizada em camadas:

### Controller

Responsável por receber requisições HTTP.

### Service

Contém as regras de negócio.

### Repository

Responsável pelo acesso aos dados.

### Database

Persistência das informações.

---

## 2. Principais Técnicas de Performance

### Paginação

Evita retornar grandes volumes de dados.

**Ferramentas:**

- Pageable
- PageRequest

### Cache

Reduz acessos repetidos ao banco de dados.

**Anotações comuns:**

- `@EnableCaching`
- `@Cacheable`
- `@CacheEvict`

### Pool de Conexões

Gerencia conexões de forma eficiente.

**Ferramenta padrão:**

- HikariCP

### Consultas Otimizadas

Evitar:

- SELECT *

Priorizar:

- Projeções
- DTOs
- Queries específicas

### Resolver o Problema N+1

**Estratégias:**

- JOIN FETCH
- EntityGraph
- Consultas customizadas

### Processamento Assíncrono

Permite executar tarefas sem bloquear a thread principal.

**Recursos:**

- `@Async`
- `CompletableFuture`

---

## 3. Observabilidade

### Spring Boot Actuator

Métricas e monitoramento.

### Micrometer

Coleta de métricas.

### Prometheus

Armazenamento de métricas.

### Grafana

Visualização de dashboards.

---

## 4. Boas Práticas para APIs Performáticas

- Utilizar DTOs.
- Implementar paginação.
- Aplicar cache quando necessário.
- Evitar consultas desnecessárias.
- Monitorar métricas continuamente.
- Utilizar índices adequados no banco.
- Tratar exceções globalmente.
- Versionar APIs.
- Utilizar logs estruturados.
- Implementar testes de carga.

---

# Glossário

| Termo | Definição |
|---------|------------|
| API REST | Interface baseada em recursos acessados via HTTP |
| DTO | Objeto utilizado para transferência de dados |
| JPA | Especificação Java para persistência |
| Hibernate | Implementação mais utilizada de JPA |
| Cache | Armazenamento temporário para acesso rápido |
| Actuator | Módulo do Spring Boot para monitoramento |
| Micrometer | Biblioteca de métricas |
| N+1 Query | Problema causado por múltiplas consultas desnecessárias |
| HikariCP | Pool de conexões padrão do Spring Boot |
| Observabilidade | Capacidade de monitorar e entender o comportamento da aplicação |

---

# Prompts Reutilizáveis

## Revisão Técnica

> Resuma os principais conceitos de APIs performáticas com Spring Boot em tópicos objetivos.

## Preparação para Entrevistas

> Gere 20 perguntas técnicas sobre Spring Boot, JPA, Cache e Performance com respostas comentadas.

## Arquitetura

> Analise a arquitetura de uma API REST em Spring Boot e sugira melhorias de escalabilidade.

## Banco de Dados

> Identifique possíveis gargalos de performance relacionados ao JPA e proponha otimizações.

## Monitoramento

> Crie um plano de observabilidade para uma aplicação Spring Boot em produção utilizando Actuator, Prometheus e Grafana.

---

# Conclusão

O uso do NotebookLM permitiu consolidar conteúdos de múltiplas fontes em um único ambiente de estudo, facilitando a exploração de conceitos complexos relacionados à construção de APIs performáticas com Spring Boot.

Além de aprofundar conhecimentos técnicos, o projeto demonstrou a importância da engenharia de prompts para obter respostas mais precisas, contextualizadas e aplicáveis a cenários reais de desenvolvimento backend.
