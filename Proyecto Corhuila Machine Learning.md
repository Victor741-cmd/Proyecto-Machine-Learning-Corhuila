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


---

## 2) Repositories and Links
- **Main Repository:** `[enlace]`
- **Frontend:**  
  For Frontend deployment, please refer to the corresponding repository: [analisis-academico-frontend](https://github.com/Victor741-cmd/analisis-academico-frontend)

- **Backend:**  
  For Backend deployment, please refer to the corresponding repository: [analisis-academico-backend](https://github.com/Victor741-cmd/analisis-academico-backend)


---

## 3) Architecture (Quick View)
- **Style:** Lightweight monolith (SPA frontend + single API). Simple deploys, fewer moving parts
- **Front:** React + Vite; local state (→ Zustand/RTK if needed); UI: Tailwind or MUI.  
- **Back:** Python + FastAPI; REST API.
- **DB:** Now Excel/SQLite; move to PostgreSQL + Alembic.  
- **Messaging/Jobs:** CRON/APScheduler now; Celery + RabbitMQ/SQS later.
- **Observability:** Logs to stdout; Prometheus metrics; Grafana; (OTel optional). 
- **Security:** Restrictive CORS; JWT / API Keys; WAF when public.
- **Gateway:** Nginx reverse proxy; basic rate limit; (future: API Gateway/BFF).

