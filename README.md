Paso 1: Dockerizar la Base de Datos
Ejecuta el siguiente comando para levantar un contenedor de MySQL:
docker run -d --name restaurante-mysql -e MYSQL_ROOT_PASSWORD=12345 -p 3306:3306 -v test_vol:/var/lib/mysql mysql:latest 

Paso 2: Navega al directorio del proyecto y ejecuta
gradlew clean build

Paso 3 :Levantar la Aplicación con Docker Compose:
docker-compose up --build

Paso 4: Probar la API
Con la aplicación corriendo, puedes acceder a la documentación Swagger en:

http://localhost:8080/swagger-ui.html
