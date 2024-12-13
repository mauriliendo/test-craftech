Despliegue Dockerizado - Django y React
Este directorio contiene el despliegue dockerizado de una aplicación web compuesta por un backend en Django y un frontend en React.js. Ambos servicios están configurados para funcionar juntos en un entorno de Docker utilizando docker-compose.

Instrucciones para probar localmente
Clona el repositorio y navega a la carpeta 2-Django-React:

bash
Copiar código
git clone https://github.com/mauriliendo/test-craftech.git
cd test-craftech/2-Django-React
Construye y ejecuta los contenedores con Docker Compose:

bash
Copiar código
docker-compose up --build
Accede a la aplicación:

El frontend de React estará disponible en http://localhost:3000.
El backend de Django estará disponible en http://localhost:8000.
Para verificar que el backend de Django está funcionando correctamente, puedes acceder a la siguiente URL para un endpoint de salud:

bash
Copiar código
http://localhost:8000/api/health
Despliegue Automático con GitHub Actions
He configurado un flujo de trabajo de GitHub Actions para desplegar la aplicación en Azure Kubernetes Service (AKS) de manera automática. Cada vez que se haga un cambio en el código del frontend (por ejemplo, en los archivos HTML), el flujo de trabajo se activa, construye la nueva imagen de Docker y despliega la actualización en AKS.

Elegí AKS para este despliegue debido a que no cuento con una cuenta en AWS ni en GCP, pero este proceso puede ser adaptado a otras plataformas de Kubernetes si es necesario.