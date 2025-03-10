# Imagen base de Java
FROM openjdk:22-jdk-slim

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo JAR del API Gateway
COPY target/api-gateway-0.0.1-SNAPSHOT.jar app.jar

# Exponer el puerto del API Gateway (8080)
EXPOSE 8080

# Comando para ejecutar el API Gateway
ENTRYPOINT ["java", "-jar", "app.jar", "--spring.profiles.active=docker"]
