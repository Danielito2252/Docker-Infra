# 🐳 Infrastructure as Code (IaC) - Docker Orchestration

🗂️ **Repositorio 5 de 5** | Ecosistema de Automatización e Ingeniería de Software

[![Docker](https://img.shields.io/badge/Docker-Infrastructure_as_Code-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/Docker_Compose-Orchestration-2496ED?style=for-the-badge)](https://docs.docker.com/compose/)
[![Environment](https://img.shields.io/badge/Environment-Isolated_DevSecOps-brightgreen?style=for-the-badge)](https://en.wikipedia.org/wiki/DevSecOps)

---

## 📝 Descripción del Proyecto

Este repositorio representa el **núcleo de infraestructura y operaciones (Ops)** de todo el ecosistema. Mediante el enfoque de **Infraestructura como Código (IaC)**, se centraliza, empaqueta y orquesta el despliegue de las herramientas utilizadas en los repositorios previos.

A través de Docker, garantizamos que el servidor de integración continua (**Jenkins**) y el motor de pruebas automatizadas (**Cypress**) se ejecuten en contenedores completamente aislados, inmutables y portables, eliminando el clásico problema de *"en mi máquina sí funciona"*.

---

## 📐 Arquitectura de Contenedores Orquestados

El archivo `docker-compose.yml` de este repositorio levanta de forma coordinada los siguientes servicios sobre una red virtual aislada (`devsecops-network`):

1. **`jenkins-ci` (Servidor de Automatización):** Corre la versión LTS de Jenkins sobre JDK 17, mapeando puertos locales y exponiendo el socket de Docker para permitir flujos "Docker-outside-of-Docker" (necesario para nuestro pipeline de DevSecOps).
2. **`cypress-runner` (Suite de QA):** Imagen oficial de Cypress preconfigurada con todas las dependencias del sistema operativo listas para ejecutar pruebas E2E sin instalaciones locales adicionales.

---

## 🚀 Guía de Despliegue Rápido

Para replicar y levantar toda la infraestructura de este proyecto universitario en cualquier computadora, solo se requieren dos comandos en la terminal:

```bash
# 1. Clonar el repositorio
git clone [https://github.com/Danielito2252/docker-infra.git](https://github.com/Danielito2252/docker-infra.git)
cd docker-infra

# 2. Levantar toda la infraestructura en segundo plano
docker compose up -d