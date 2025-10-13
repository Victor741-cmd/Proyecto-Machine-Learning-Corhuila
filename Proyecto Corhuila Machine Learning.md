# Machine Learning Project


## 1) Summary 
This research project aims to analyze the performance in critical reading competence of Systems Engineering students at the Corporación Universitaria del Huila – CORHUILA during the 2025 Saber-Pro tests, using Machine Learning techniques.

The study seeks to identify the predictive variables that influence students’ results, determine the most effective pedagogical strategies, and evaluate the didactic impact of applying Machine Learning models to enhance academic performance in critical reading.

Through a quantitative and empirical-analytical approach, predictive models are developed to understand how teaching strategies and individual factors affect the development of critical reading skills, contributing to the improvement of teaching and learning processes in higher education.

**General Objective**
Develop a machine learning model using ML techniques to analyze the performance of the Saber Pro 2025 tests in the critical reading competence of engineering students at Corhuila University, in order to identify areas for continuous improvement.

**Specific Objectives**
- **O1.** Establish ML models focused on the performance of the Saber Pro 2021 tests for engineering students at Corhuila University.
- **O2.** Identify best practices used by students with the highest performance in the critical reading competence.
- **03.** Develop a machine learning model that predicts the performance in the critical reading competence of engineering students at Corhuila University.

- **Métricas (KPI):** % disponibilidad, tiempo de respuesta, NPS, etc.

---

## 2) Repositorios y Enlaces
- **Repositorio principal (mono/meta):** `[enlace]`
- **Frontend:**  
  For Frontend deployment, please refer to the corresponding repository: [analisis-academico-frontend](https://github.com/Victor741-cmd/analisis-academico-frontend)

- **Backend:**  
  For Backend deployment, please refer to the corresponding repository: [analisis-academico-backend](https://github.com/Victor741-cmd/analisis-academico-backend)



> **Regla:** cada repo debe tener su propio `README.md` con: propósito, cómo correr local, variables de entorno, tests y pipeline.

---

## 3) Arquitectura (Vista Rápida)
- **Estilo:** monolito / microservicios / eventos / serverless / híbrido.  
- **Front:** framework / gestor de estado / librería UI.  
- **Back:** lenguaje / framework / API (REST/GraphQL/gRPC).  
- **BD:** PostgreSQL/MySQL/NoSQL + estrategia de migraciones.  
- **Mensajería/Jobs:** Kafka/Rabbit/SQS/CRON.  
- **Observabilidad:** logs, métricas, trazas (ELK/Prom/Grafana).  
- **Seguridad:** OAuth2/OIDC, JWT, API Keys, WAF.  
- **Gateway:** API-Gateway/BFF, rate limit, CORS, circuit breaker.

---

## 4) Entornos y Variables
| Entorno | URL base | Rama | BD | Observabilidad |
|---|---|---|---|---|
| Local | `http://localhost` | feature/* | docker | consola local |
| DEV | `https://dev...` | `develop` | dev-db | dev-grafana |
| QA  | `https://qa...`  | `qa`      | qa-db  | qa-grafana  |
| STG | `https://stg...` | `release/*` | stg-db | stg-grafana |
| PRD | `https://...`    | `main`    | prd-db | prd-grafana |

---

## 5) Flujo de Desarrollo y Branching
- **Commits:** Conventional Commits (feat, fix, docs, chore, refactor, perf, test, build, ci).  
- **Ramas:**
  - `main` → producción
  - `develop` → integración continua
  - `feature/*` → nuevas features
  - `hotfix/*` → correcciones urgentes
  - `release/x.y.z` → preparación de release

---

## 6) Configuración Local (Dev)
**Requisitos:** Node X / Java Y / Go Z, Docker, Docker Compose, Make, Git.

```bash
# 1) clonar
git clone <repo>
cd <repo>

# 2) preparar
cp .env.example .env
docker compose up -d

# 3) instalar frontend
cd frontend && npm i && npm run dev

# 4) backend
cd ../backend && make dev
```

---

## 7) Calidad: Lint, Tests y Cobertura
```bash
npm run lint
npm test -- --watch=false
npm run test:e2e
npm run coverage
```

**Políticas:** cobertura mínima, PR bloquea si falla.

---

## 8) Seguridad y Cumplimiento
- **Autenticación:** OAuth2/OIDC o JWT.  
- **Autorización:** RBAC/ABAC.  
- **Secretos:** Vault o KeyVault.  
- **CORS:** dominios permitidos.  
- **Auditoría:** log de acción.

---

## 9) API Gateway y Servicios
Un único punto de entrada con: rate-limit, auth, circuit-breaker, observabilidad.

Rutas ejemplo:
```
/api/v1/auth/*      → svc-security
/api/v1/schedule/*  → svc-schedule
/api/v1/assets/*    → svc-assets
```

---

## 10) CI/CD
- **Pipelines:** build → lint/tests → scan → artifact → deploy.  
- **Despliegue:** blue/green o rolling.  
- **Rollback:** versión anterior empaquetada.

---

## 11) Monitoreo, Alertas y Mantenimiento
- **Logs:** correlación por trace_id.  
- **Métricas:** latencia, errores, throughput.  
- **Alertas:** on-call y umbrales.  
- **Tareas:** limpieza, backups, rotación de logs.

---

## 12) Contribución
- **PRs:** build/test ok, cobertura ≥ X%, lint ok, revisores.  
- **Issues:** reproducibles con plantilla.  
- **Código de conducta.**

---

# Ejemplo: Proyecto "Gestión Laboratorio (CORHUILA)"

## Resumen
Prototipo funcional para la **gestión de laboratorios** en CORHUILA (sede Prado Alto): reservas, inventario, actividades y usuarios.

**KPI:**  
- Reserva < 2 min  
- Disponibilidad > 99.5%  
- Conflictos de agenda -30%

---

## Repositorios
- **Documentación:** https://github.com/code-corhuila/laboratory-management.git  
- **Agenda:** https://github.com/code-corhuila/schedule-management.git  
- **Hoja de Vida:** https://github.com/code-corhuila/equipment-lifecycle-management.git  
- **Frontend:** https://github.com/code-corhuila/frontend-laboratory-management.git  
- **Seguridad:** https://github.com/code-corhuila/backend-security

---

## Arquitectura
- **Front:** SPA JS moderna.  
- **Back:** microservicios (seguridad, agenda, hoja de vida).  
- **BD:** PostgreSQL + migraciones.  
- **Gateway:** API Gateway con auth y monitoreo.

Rutas tipo:
```
/api/v1/auth/*           → backend-security
/api/v1/schedule/*       → backend-schedule-management
/api/v1/equipment/*      → backend-equipment-lifecycle-management
```

---

## Entornos
| Entorno | Rama | Gateway |
|---|---|---|
| DEV | `develop` | `https://dev-gw.corhuila.edu` |
| QA  | `qa`      | `https://qa-gw.corhuila.edu`  |
| STG | `release/*` | `https://stg-gw.corhuila.edu` |
| PRD | `main`    | `https://gw.corhuila.edu`     |

---

## Roadmap
- Fase 1: reservas, catálogo, auth.  
- Fase 2: calendario avanzado, reportes.  
- Fase 3: analítica de uso e integración académica.

