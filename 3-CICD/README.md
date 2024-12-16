# **CI/CD - NGINX Dockerizado**

Este directorio contiene la configuración de CI/CD para una aplicación que utiliza **NGINX** como servidor web. Cada vez que se realice un cambio en el archivo `index.html`, se construirá y desplegará automáticamente una nueva imagen de Docker.

---

## **Instrucciones para Probar Localmente**

1. **Clona el repositorio y navega a la carpeta `3-CICD`:**
   ```bash
   git clone https://github.com/mauriliendo/test-craftech.git
   cd test-craftech/3-CICD
   ```

2. **Construye y ejecuta los contenedores con Docker Compose:**
   ```bash
   docker-compose up --build
   ```

3. **Accede a la aplicación:**
   - Si estás ejecutando en tu máquina local, abre tu navegador y ve a:  
     `http://localhost:80`
   - Si tienes la IP pública del contenedor, accede a:  
     `http://<IP_PUBLICA>:80`

---

## **Despliegue Automático con GitHub Actions**

He configurado un flujo de trabajo de **GitHub Actions** denominado `deployNginx`. Este flujo de trabajo permite que cualquier cambio en el archivo `index.html` dispare automáticamente el proceso de:

1. **Construcción** de una nueva imagen de Docker para NGINX.
2. **Despliegue** de la imagen en **Azure Kubernetes Service (AKS)**.

### **Razón para Elegir AKS**

He optado por usar **AKS** para esta implementación ya que no cuento con una cuenta en AWS ni en GCP. Sin embargo, este flujo de trabajo puede adaptarse fácilmente a otras plataformas de Kubernetes si lo deseas.

---

## **Adaptabilidad del Flujo de Trabajo**

El flujo de trabajo `deployNginx` puede ser modificado para ajustarse a otras plataformas como:

- **Amazon Elastic Kubernetes Service (EKS)**
- **Google Kubernetes Engine (GKE)**
- **Plataformas de Kubernetes locales**

---

## **Licencia**

Este proyecto está licenciado bajo la [MIT License](LICENSE).