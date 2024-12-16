# **Proyecto de Prueba Técnica**

Este repositorio contiene una solución que incluye varios componentes clave de infraestructura y desarrollo. El objetivo es proporcionar una implementación de una aplicación web completa, junto con un sistema de CI/CD automatizado y despliegue utilizando Docker y Kubernetes.

---

## **Descripción**

El proyecto está dividido en varias pruebas que abarcan desde la creación de un diagrama de red hasta la implementación de una aplicación Django y React.js con un sistema de integración y entrega continua (CI/CD). La solución es totalmente dockerizada para facilitar su despliegue tanto en entornos locales como en la nube (Azure, AWS, GCP, etc.).

---

## **Prueba 1 - Diagrama de Red**

Se ha diseñado un diagrama de red para una aplicación web que cubre las siguientes características:

- **Cargas variables**
- **Alta disponibilidad (HA)**
- **Frontend** en JavaScript
- **Backend** con base de datos relacional y no relacional
- **Consumo de dos microservicios externos**

El diagrama y su justificación están disponibles en el repositorio, detallando las decisiones tomadas en cuanto a la arquitectura y los servicios utilizados.

---

## **Prueba 2 - Despliegue de la Aplicación**

La aplicación está compuesta por:

- **Backend** en Django
- **Frontend** en React.js

Ambos servicios están dockerizados y se orquestan mediante un archivo `docker-compose` para facilitar su despliegue en un solo entorno. Este despliegue se puede realizar tanto en una PC local como en la nube.

Los archivos `Dockerfile` para el backend y frontend están presentes en el repositorio, junto con las instrucciones detalladas para compilar y ejecutar la aplicación.

---

## **Prueba 3 - CI/CD**

Se ha implementado un pipeline de CI/CD que permite:

- **Construir y actualizar automáticamente** la imagen de un contenedor NGINX.
- Ante cualquier cambio realizado en el archivo `index.html`, la nueva imagen se construye y despliega en la plataforma elegida.

El pipeline se ha configurado para ejecutarse en una plataforma de CI de elección (como GitHub Actions, GitLab CI, etc.).

---

## **Instrucciones para Clonar y Ejecutar el Proyecto**

1. Clona este repositorio:
   ```bash
   git clone <url-del-repositorio>
   ```

2. Accede al directorio del proyecto:
   ```bash
   cd <nombre-del-repositorio>
   ```

3. Construye y ejecuta los contenedores:
   ```bash
   docker-compose up --build
   ```

---

## **Contribución**

Las contribuciones son bienvenidas. Si deseas contribuir, por favor sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una rama para tu funcionalidad o bugfix:
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```
3. Haz un commit de tus cambios:
   ```bash
   git commit -m "Agrega una nueva funcionalidad"
   ```
4. Sube los cambios a tu rama:
   ```bash
   git push origin feature/nueva-funcionalidad
   ```
5. Abre un pull request.

---

## **Licencia**

Este proyecto está licenciado bajo la [MIT License](LICENSE).
