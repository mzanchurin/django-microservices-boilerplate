# Django Microservices Boilerplate

Production-ready boilerplate for building microservices with Django and Django REST Framework.  
Includes an API Gateway, separate services, centralized authentication, background jobs, and Docker-based deployment.

## What’s inside

- **API Gateway**
  - Single entry point for all client requests
  - Request routing to internal services
  - JWT validation and basic rate limiting hooks

- **Auth Service**
  - JWT-based authentication (access/refresh tokens)
  - User registration & login
  - Password reset hooks / stubs for email

- **User Service**
  - User profile management
  - Separation of auth data and profile data
  - Ready for extension with domain-specific fields

- **Notification Service**
  - Async sending of emails / notifications via Celery
  - Redis as a broker
  - Unified interface for other services to push notifications

- **Celery Workers + Redis**
  - Background jobs for notifications and long-running tasks
  - Centralized task configuration for all services

- **Dockerized Environment**
  - `docker-compose` for local development
  - Separate containers for gateway, services, workers, Redis
  - Environment-based configuration (dev / prod)

## Tech stack

- **Backend:** Django, Django REST Framework  
- **Async / Tasks:** Celery, Redis  
- **Auth:** JWT (access & refresh tokens)  
- **Infrastructure:** Docker, docker-compose  

This boilerplate is meant as a starting point for real-world microservice architectures with Django: clear boundaries between services, an API Gateway, background processing, and a project structure that can grow with your application.

