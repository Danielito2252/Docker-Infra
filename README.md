# 🐳 Docker Infrastructure as Code (IaC)

### Infraestructura DevSecOps para Jenkins, Cypress y OWASP ZAP

> Entorno reproducible basado en Docker Compose para ejecutar pipelines CI/CD, pruebas automatizadas E2E y análisis de seguridad dinámica (DAST).

---

## 📋 Descripción

Este repositorio contiene la infraestructura como código (IaC) necesaria para desplegar un ecosistema completo de automatización y seguridad.

Con un único comando es posible aprovisionar:

* ⚙️ Jenkins CI Server
* 🧪 Entorno de ejecución Cypress
* 🔒 OWASP ZAP para análisis DAST
* 🌐 Red privada Docker para comunicación segura

---

## 🏗️ Arquitectura

```text
┌─────────────┐
│   GitHub    │
└──────┬──────┘
       │ Webhook
       ▼
┌─────────────┐
│   Jenkins   │
└──────┬──────┘
       │
 ┌─────┴─────┐
 │           │
 ▼           ▼
Cypress   OWASP ZAP
(E2E)      (DAST)
```

---

## ⚙️ Servicios Desplegados

| Servicio          | Propósito                            |
| ----------------- | ------------------------------------ |
| 🏗️ Jenkins       | Orquestación de pipelines CI/CD      |
| 🧪 Cypress        | Ejecución de pruebas automatizadas   |
| 🔒 OWASP ZAP      | Escaneo de vulnerabilidades DAST     |
| 🌐 Docker Network | Comunicación aislada entre servicios |

---

## 🚀 Despliegue

Levantar toda la infraestructura:

```bash
docker compose up -d
```

Verificar contenedores activos:

```bash
docker ps
```

Consultar logs de Jenkins:

```bash
docker logs jenkins-ci
```

Detener el entorno:

```bash
docker compose down
```

---

## 📊 Evidencias

### 🔄 Pipeline DevSecOps



images/stage-view-success.png


---

### 🧪 Resultados de Cypress




images/cypress-run.png


---

### 🔒 Reporte DAST



images/zap-report.png


---

## 🔗 Ecosistema Relacionado

| Proyecto                   | Función                   |
| -------------------------- | ------------------------- |
| Jenkins-DevSecOps-Pipeline | Orquestación principal    |
| Cypress-E2E-Suite          | Automatización funcional  |
| Cypress-Framework          | Framework de pruebas      |
| TuleApp-QA-Workflow        | Gestión y trazabilidad QA |

---

## 📁 Estructura del Proyecto

```text
.
├── docker-compose.yml
├── jenkins_home/
├── docs/
│   └── images/
└── README.md
```

---

## 🎯 Beneficios

✅ Infraestructura reproducible

✅ Despliegue en segundos

✅ Integración DevSecOps

✅ Automatización E2E

✅ Escaneo de vulnerabilidades

✅ Fácil mantenimiento

---

## 👨‍💻 Autor

**Herberth Barrios**

🔗 GitHub: https://github.com/Danielito2252

🔗 LinkedIn: https://www.linkedin.com/in/herberth-barrios-299236261/

---

## 📄 Licencia

Distribuido bajo la licencia **MIT License**.
