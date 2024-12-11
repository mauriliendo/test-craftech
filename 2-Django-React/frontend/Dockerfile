# Usar una imagen base de Node para construir la aplicación React
FROM node:18-alpine AS build

# Establecer directorio de trabajo
WORKDIR /app

# Copiar archivos de dependencias
COPY frontend/package.json frontend/package-lock.json ./

# Instalar dependencias
RUN npm install

# Copiar código fuente
COPY frontend/ .

# Construir la aplicación
RUN npm run build

# Imagen final con Nginx para servir la aplicación
FROM nginx:alpine

# Copiar los archivos de construcción al directorio de Nginx
COPY --from=build /app/build /usr/share/nginx/html

# Exponer puerto 80
EXPOSE 80

# Comando por defecto de Nginx
CMD ["nginx", "-g", "daemon off;"]