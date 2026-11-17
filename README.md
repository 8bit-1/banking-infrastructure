# 🏦 Banking Infrastructure

Repositorio de infraestructura del sistema bancario basado en microservicios. Contiene la configuración de todos los servicios de soporte necesarios para correr el sistema completo.

## 📦 Servicios incluidos

| Servicio | Descripción | Puerto |
|---|---|---|
| PostgreSQL 15 | Base de datos relacional principal | 5432 |
| Redis 7.2 | Caché en memoria | 6379 |
| RabbitMQ 3.12 | Broker de mensajería asíncrona | 5672 / 15672 |
| Keycloak 23 | Servidor de autenticación OAuth2/JWT | 8080 |
| Zipkin 3 | Trazabilidad distribuida | 9411 |
| Prometheus | Recolección de métricas | 9090 |
| Grafana | Dashboards de monitoreo | 3000 |

## 🛠️ Requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## 🚀 Levantar la infraestructura

```bash
# Clonar el repositorio
git clone https://github.com/TU_USUARIO/banking-infrastructure
cd banking-infrastructure

# Levantar todos los servicios
docker compose up -d

# Verificar que todo esté corriendo
docker compose ps
```

## 🌐 Paneles de administración

| Servicio | URL | Usuario | Contraseña |
|---|---|---|---|
| Keycloak | http://localhost:8080 | admin | admin123 |
| RabbitMQ | http://localhost:15672 | admin | admin123 |
| Prometheus | http://localhost:9090 | — | — |
| Grafana | http://localhost:3000 | admin | admin123 |
| Zipkin | http://localhost:9411 | — | — |

## 📁 Estructura del repositorio

```
banking-infrastructure/
├── docker-compose.yml        → Definición de todos los contenedores
└── infrastructure/
    └── prometheus.yml        → Configuración de scraping de métricas
```

## 🔧 Comandos útiles

```bash
# Ver logs de todos los servicios
docker compose logs -f

# Ver logs de un servicio específico
docker compose logs -f postgres

# Apagar todos los servicios
docker compose down

# Apagar y eliminar volúmenes (borra todos los datos)
docker compose down -v

# Ver consumo de recursos
docker stats
```

## 🗂️ Repositorios relacionados

- [banking-config-server](https://github.com/TU_USUARIO/banking-config-server)
- [banking-gateway](https://github.com/TU_USUARIO/banking-gateway)
- [banking-user-service](https://github.com/TU_USUARIO/banking-user-service)
- [banking-account-service](https://github.com/TU_USUARIO/banking-account-service)
- [banking-transaction-service](https://github.com/TU_USUARIO/banking-transaction-service)
- [banking-notification-service](https://github.com/TU_USUARIO/banking-notification-service)


.