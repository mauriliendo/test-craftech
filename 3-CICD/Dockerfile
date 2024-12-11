# Usamos la imagen oficial de NGINX
FROM nginx:latest

# Copiamos nuestro index.html al contenedor
COPY index.html /usr/share/nginx/html/index.html

# Exponemos el puerto 80 para acceder al servidor
EXPOSE 80

# Iniciamos el servidor NGINX
CMD ["nginx", "-g", "daemon off;"]
