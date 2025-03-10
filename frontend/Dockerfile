# Etapa 1: Construcción de la aplicación
FROM node:20 as build

# Establecer directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar los archivos de configuración del proyecto
COPY package.json package-lock.json ./


# Instalar las dependencias
RUN npm install --frozen-lockfile

# Copiar el resto del código fuente
COPY . .

# Construir la aplicación con Vite
RUN npm run build

# Etapa 2: Servir la aplicación con Nginx
FROM nginx:1.23

# Copiar los archivos de la build al directorio de Nginx
COPY --from=build /app/dist /usr/share/nginx/html

# Copia la configuración de Nginx
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Exponer el puerto 80 para servir la aplicación
EXPOSE 80

# Iniciar Nginx
CMD ["nginx", "-g", "daemon off;"]
