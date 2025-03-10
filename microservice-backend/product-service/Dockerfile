# Imagen base de Java
FROM openjdk:22-jdk-slim

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo JAR del microservicio
COPY target/product-service-0.0.1-SNAPSHOT.jar app.jar

# Exponer el puerto del servicio (cambia según corresponda)
EXPOSE 9010

# Comando para ejecutar el microservicio
ENTRYPOINT ["java", "-jar", "app.jar", "--spring.profiles.active=docker"]
