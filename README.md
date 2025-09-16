### 1. 🎯 Problem Statement and Context


❌ Lambda NÃO permitido
❌ Monólitos NÃO permitidos
❌ Single AZ NÃO permitido
❌ Ionic NÃO permitido
✅ Mobile nativo apenas (Swift ou Kotlin)
❌ MongoDB NÃO permitido
❌ Apenas uma base relacional NÃO é permitido
✅ podemos usar múltiplas bases relacionais??
❌ Outras clouds NÃO permitidas
✅ apenas AWS

--------

Cadastro de POCs
Busca de POCs por nome, linguagem e tags
Multi-tenancy (vários clientes isolados na mesma plataforma)
Autenticação segura (login e controle de sessão)
Geração de relatórios
Geração de vídeos com os POCs do ano
Suporte a sessões em tempo real (dojos)


Recomended Reading: http://diego-pacheco.blogspot.com/2021/10/breaking-problems-down.html

### 2. 🎯 Goals

```
Mobile App nativo:
Swift (iOS) ou Kotlin (Android), com build pipelines separados
Backend distribuído em microsserviços sobre ECS Fargate ou EKS, seguindo o modelo RESTful
Base de dados relacional única: PostgreSQL no Amazon RDS com suporte a multi-tenant (via tenant_id)
Autenticação e autorização com Amazon Cognito (com suporte a login federado)
Geração de relatórios com serviço containerizado (e.g., Java + JasperReports ou Node.js + PDFKit)
Geração de vídeos com FFmpeg rodando em batch container (Fargate) salvando o resultado em S3
Real-time Dojos com WebSockets sobre API Gateway conectado a serviço backend stateful (via Redis para sessões)
Busca textual e por tags via ILIKE, índices em PostgreSQL, e filtragem em backend (sem uso de Elastic ou Mongo)
Armazenamento de arquivos em Amazon S3 (relatórios e vídeos)
Observabilidade com CloudWatch, X-Ray, e alarmes no SNS
```
Recommended Learning: http://diego-pacheco.blogspot.com/2020/05/education-vs-learning.html

### 3. 🎯 Non-Goals

```

```
Recommended Reading: http://diego-pacheco.blogspot.com/2021/01/requirements-are-dangerous.html

### 📐 3. Principles


Example:

```

### 🏗️ 4. Overall Diagrams

<img width="653" height="971" alt="image" src="https://github.com/user-attachments/assets/7d49ad08-077b-4ab6-80de-a2fc3983d040" />


### 🧭 5. Trade-offs

List the tradeoffs analysis, comparing pros and cons for each major decision.
Before you need list all your major decisions, them run tradeoffs on than.
example:
Major Decisions: 
```
1. One mobile code base - should be (...)
2. Reusable capability and low latency backends should be (...)
3. Cache efficiency therefore should do (...)
```
Tradeoffs:
```
1. React Native vs (Flutter and Native)
2. Serverless vs Microservices
3. Redis vs Enbeded Caches
```
Each tradeoff line need to be:
```
PROS (+) 
  * Benefit: Explanation that justify why the benefit is true.
CONS (+)
  * Problem: Explanation that justify why the problem is true.
```
PS: Be careful to not confuse problem with explanation. 
<BR/>Recommended reading: http://diego-pacheco.blogspot.com/2023/07/tradeoffs.html

### 🌏 6. For each key major component

What is a majore component? A service, a lambda, a important ui, a generalized approach for all uis, a generazid approach for computing a workload, etc...
```
6.1 - Class Diagram              : classic uml diagram with attributes and methods
6.2 - Contract Documentation     : Operations, Inputs and Outputs
6.3 - Persistence Model          : Diagrams, Table structure, partiotioning, main queries.
6.4 - Algorithms/Data Structures : Spesific algos that need to be used, along size with spesific data structures.
```

Exemplos of other components: Batch jobs, Events, 3rd Party Integrations, Streaming, ML Models, ChatBots, etc... 

Recommended Reading: http://diego-pacheco.blogspot.com/2018/05/internal-system-design-forgotten.html

### 🖹 7. Migrations

IF Migrations are required describe the migrations strategy with proper diagrams, text and tradeoffs.

### 🖹 8. Testing strategy

Explain the techniques, principles, types of tests and will be performaned, and spesific details how to mock data, stress test it, spesific chaos goals and assumptions.

### 🖹 9. Observability strategy

Explain the techniques, principles,types of observability that will be used, key metrics, what would be logged and how to design proper dashboards and alerts.

### 🖹 10. Data Store Designs

For each different kind of data store i.e (Postgres, Memcached, Elasticache, S3, Neo4J etc...) describe the schemas, what would be stored there and why, main queries, expectations on performance. Diagrams are welcome but you really need some dictionaries.

### 🖹 11. Technology Stack

Describe your stack, what databases would be used, what servers, what kind of components, mobile/ui approach, general architecture components, frameworks and libs to be used or not be used and why.

### 🖹 12. References

* Architecture Anti-Patterns: https://architecture-antipatterns.tech/
* EIP https://www.enterpriseintegrationpatterns.com/
* SOA Patterns https://patterns.arcitura.com/soa-patterns
* API Patterns https://microservice-api-patterns.org/
* Anti-Patterns https://sourcemaking.com/antipatterns/software-development-antipatterns
* Refactoring Patterns https://sourcemaking.com/refactoring/refactorings
* Database Refactoring Patterns https://databaserefactoring.com/
* Data Modelling Redis https://redis.com/blog/nosql-data-modeling/
* Cloud Patterns https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/introduction.html
* 12 Factors App https://12factor.net/
* Relational DB Patterns https://www.geeksforgeeks.org/design-patterns-for-relational-databases/
* Rendering Patterns https://www.patterns.dev/vanilla/rendering-patterns/
* REST API Design https://blog.stoplight.io/api-design-patterns-for-rest-web-services
