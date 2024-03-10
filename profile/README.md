# FIAP Pós Tech - Software Architecture - Tech Challenge 
Repositories for the "Tech Challenge" group project (2023 SOAT1 Group 63) from FIAP Pós Tech's [Software Architecture course](https://postech.fiap.com.br/curso/software-architecture/).

## Project
The project goal was to study software architecture related topics by creating a self-service and kitchen managment service for a fictional restaurant.

The client may identifiy itself; Checkout an order; Confirm it; Pay it via an external payment service, and the order could be then processed by the kitchen employees.

## Phases

The project and the course itself are divided in several 'phases' each one covering some software architecture-related topics.
Some of these topics required code rewriting, refactoring and repository splitting.

Therefore there are releases in each repo for each phase they were relevant and what topics were covered in them.

### Phase 1

  - Monolithic Spring Boot application with PostgreSQL
  - Hexagonal (Ports and Adapters) architecture
  - Domain Driver Design brainstorming

<details>
  <summary>DDD diagrams</summary>

  ![Phase 1 DDD](https://github.com/soat-tech-challenge/.github/assets/44736064/72b12aaf-4b68-48b6-a40b-e130368e0e82)

</details>

  - `Dockerfile` and `docker-compose.yml` files created

### Phase 2

  - Replaced `docker-compose.yml` with Kubernetes config
  - Project rewritten using Clean architecture

### Phase 3

  - Refactored project for use within AWS
    - Created Lambda identification flow (JWT auth)
  - Created initial Terraform files, for use with Terraform Cloud
  - Set up Github Actions workflows
    - Maven build and semver bump
    - Push/Deploy to Docker Hub and AWS
    - Terraform Cloud remote plan, apply and destroy

  ![Phase 3 Client flow AWS diagram](https://github.com/soat-tech-challenge/.github/assets/44736064/00a0f09e-daea-42d1-9354-cab56afac24e)

### Phase 4

  - Backend was split into 4 microservices
    - Two of them now use DynamoDB instead of PostgreSQL
  - Sonarcloud set up. For Maven projects CI-based analysis was used (for Java code coverage via Jacoco)
  - Unit and behavior tests were created using Cucumber and JUnit.
  - Terraform files modified for use with Vocareum Labs via AWS Academy, provided by the course.

  ![Phase 4 Client flow AWS diagram](https://github.com/soat-tech-challenge/.github/assets/44736064/92aee4bb-f2a0-41c1-8f7b-b3ee3a4a27b1)

### Phase 5

  - Use SAGA pattern in payment flow
    - Using AWS SQS
  - Create OWASP ZAP and LGPD RIPD reports.

## Versioning
The repos in this organization mostly follow semver, but the major version corresponds to the project's target phase at the time of commit. 
E.g: v4.X.X -> Phase 4

## Group members
- [g-otn](https://github.com/g-otn)
- [HenriqueZaim](https://github.com/HenriqueZaim)
- [marcelovbcfilho](https://github.com/marcelovbcfilho)
- [thgosii](https://github.com/thgosii)
