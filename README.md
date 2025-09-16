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

### 3. 🎯 Non-Goals

```

```

### 📐 3. Principles


Example:


### 🏗️ 4. Overall Diagrams

<img width="653" height="971" alt="image" src="https://github.com/user-attachments/assets/7d49ad08-077b-4ab6-80de-a2fc3983d040" />


### 🧭 5. Trade-offs

Major Decisions: 
```
```
Tradeoffs:

```
```

Each tradeoff line need to be:
```
PROS (+) 
CONS (+)
```

### 🌏 6. For each key major component

```
```

### 🖹 7. Migrations

### 🖹 8. Testing strategy

### 🖹 9. Observability strategy

### 🖹 10. Data Store Designs

### 🖹 11. Technology Stack

