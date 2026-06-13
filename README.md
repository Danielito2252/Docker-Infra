# 🐳 Docker Infrastructure as Code (IaC)

> Infraestructura de automatización para entornos DevSecOps utilizando Docker y Docker Compose.

<div align="center">

[![Docker](https://img.shields.io/badge/Docker-IaC-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/Docker_Compose-Orchestration-2496ED?style=for-the-badge)
](https://docs.docker.com/compose/)
[![DevSecOps](https://img.shields.io/badge/DevSecOps-Automation-brightgreen?style=for-the-badge)](https://en.wikipedia.org/wiki/DevSecOps)

</div>

---

## 📋 Resumen

Este repositorio implementa la capa de **Infraestructura como Código (IaC)** del ecosistema de automatización y calidad de software.

Mediante **Docker** y **Docker Compose**, se orquestan los servicios necesarios para ejecutar procesos de:

* ⚙️ Integración Continua (CI)
* 🚀 Automatización DevSecOps
* 🧪 Pruebas E2E con Cypress
* 📦 Entornos reproducibles y portables

Todo el entorno puede desplegarse en cualquier máquina con exactamente la misma configuración.

---

## 🏗️ Arquitectura

```text
┌─────────────────────┐
│    Docker Host      │
└──────────┬──────────┘
           │
           ▼
┌───────────────────────────────┐
│      devsecops-network        │
└───────────┬───────────┬───────┘
            │           │
            ▼           ▼

   Jenkins CI      Cypress Runner
   (Automation)      (QA E2E)
```

### Servicios desplegados

| Servicio          | Función                              |
| ----------------- | ------------------------------------ |
| 🧩 Jenkins CI     | Automatización de pipelines CI/CD    |
| 🧪 Cypress Runner | Ejecución de pruebas End-to-End      |
| 🌐 Docker Network | Comunicación aislada entre servicios |

---

## 🚀 Inicio Rápido

### Clonar repositorio

```bash
git clone https://github.com/Danielito2252/docker-infra.git

cd docker-infra
```

### Levantar infraestructura

```bash
docker compose up -d
```

---

## 🔍 Validación

Verificar contenedores activos:

```bash
docker ps
```

Consultar logs de Jenkins:

```bash
docker logs jenkins-ci
```

Detener infraestructura:

```bash
docker compose down
```

---

## 📊 Evidencias

### 🚀 Pipeline DevSecOps

> Flujo completo de integración continua y automatización.

![Pipeline Stage View](docs/images/pipeline-stage-view.png)

---

### 🔒 Análisis SAST - SonarQube

> Métricas de calidad y seguridad del código.

![SonarQube Dashboard](docs/images/sonarqube-dashboard.png)

---

## 🔗 Ecosistema Relacionado

Este proyecto sirve como base para los demás componentes del portafolio:

| Repositorio                | Función                   |
| -------------------------- | ------------------------- |
| Jenkins-DevSecOps-Pipeline | Automatización CI/CD      |
| Cypress-E2E-Suite          | Pruebas automatizadas     |
| Docker-Infrastructure      | Orquestación de servicios |

---

## 🛠️ Tecnologías

* Docker
* Docker Compose
* Jenkins LTS
* Cypress
* DevSecOps
* Infrastructure as Code (IaC)

---

## 👨‍💻 Autor

### Herberth Barrios

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-blue?style=for-the-badge\&logo=linkedin)](https://www.linkedin.com/in/herberth-barrios-299236261/)

[![GitHub](https://img.shields.io/badge/GitHub-Ver_Perfil-black?style=for-the-badge\&logo=github)](https://github.com/Danielito2252)

---

## 📄 Licencia

Distribuido bajo la Licencia MIT.
