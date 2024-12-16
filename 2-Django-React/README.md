# **Despliegue Dockerizado - Django y React**

Este directorio contiene el despliegue dockerizado de una aplicación web compuesta por un **backend en Django** y un **frontend en React.js**. Ambos servicios están configurados para funcionar juntos en un entorno de Docker utilizando **docker-compose**.

---

## **Instrucciones para Probar Localmente**

1. **Clona el repositorio y navega a la carpeta `2-Django-React`:**
   ```bash
   git clone https://github.com/mauriliendo/test-craftech.git
   cd test-craftech/2-Django-React
   ```

2. **Construye y ejecuta los contenedores con Docker Compose:**
   ```bash
   docker-compose up --build
   ```

3. **Accede a la aplicación:**
   - El frontend de **React** estará disponible en:  
     `http://localhost:3000`
   - El backend de **Django** estará disponible en:  
     `http://localhost:8000`

4. **Verifica el estado del backend:**
   - Puedes usar el siguiente endpoint de salud para comprobar que el backend está funcionando correctamente:
     ```
     http://localhost:8000/api/health
     ```

---

## **Despliegue Automático con GitHub Actions**

He configurado un flujo de trabajo de **GitHub Actions** para desplegar la aplicación en **Azure Kubernetes Service (AKS)** de manera automática. Este flujo de trabajo se activa cada vez que se realizan cambios en el código del frontend (por ejemplo, en los archivos HTML). 

### **Proceso de Despliegue:**

1. **Construcción** de las imágenes de Docker para el frontend y el backend.
2. **Despliegue** de las imágenes actualizadas en **AKS**.

### **Razón para Elegir AKS**

He optado por usar **AKS** debido a la disponibilidad de recursos en Azure. No obstante, este flujo de trabajo puede ser adaptado para otras plataformas como AWS, GCP o incluso Kubernetes en entornos locales.

---

## **Adaptabilidad del Flujo de Trabajo**

El flujo de trabajo puede ajustarse a diferentes plataformas, incluyendo:

- **Amazon Elastic Kubernetes Service (EKS)**
- **Google Kubernetes Engine (GKE)**
- **Plataformas de Kubernetes locales**

---

## **Licencia**

Este proyecto está licenciado bajo la [MIT License](LICENSE).