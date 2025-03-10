# Imagen base de Java
FROM openjdk:22-jdk-slim

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo JAR del Service Registry
COPY target/service-registry-0.0.1-SNAPSHOT.jar app.jar

# Exponer el puerto de Eureka (8761)
EXPOSE 8761

# Comando para ejecutar el Service Registry
ENTRYPOINT ["java", "-jar", "app.jar", "--spring.profiles.active=docker"]
