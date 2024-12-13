CI/CD - NGINX Dockerizado
Este directorio contiene la configuración de CI/CD para una aplicación que utiliza NGINX como servidor web. Cada vez que se realice un cambio en el archivo index.html, se construirá y desplegará automáticamente una nueva imagen de Docker.

Instrucciones para probar localmente
Clona el repositorio y navega a la carpeta 3-CICD:

bash
Copiar código
git clone https://github.com/mauriliendo/test-craftech.git
cd test-craftech/3-CICD
Construye y ejecuta los contenedores con Docker Compose:

bash
Copiar código
docker-compose up --build
Accede a la aplicación:

Si estás ejecutando en tu máquina local, abre tu navegador y ve a http://localhost:80.
Si tienes la IP pública del contenedor, accede a http://<IP_PUBLICA>:80.
Despliegue Automático con GitHub Actions
He configurado un flujo de trabajo de GitHub Actions denominado deployNginx. Este flujo de trabajo permite que cualquier cambio en el archivo index.html dispare automáticamente el proceso de construcción y despliegue de la imagen de NGINX en Azure Kubernetes Service (AKS).

He elegido AKS para esta implementación ya que no cuento con una cuenta en AWS ni en GCP, pero este flujo de trabajo puede adaptarse a otras plataformas de Kubernetes si lo deseas.