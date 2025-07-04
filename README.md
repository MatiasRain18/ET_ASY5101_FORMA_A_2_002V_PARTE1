# ET_ASY5101_FORMA_A_2_002V_PARTE1

## Grupo 6 - Evaluación 2 - Integración de Plataformas

**Integrantes:**
- Matías Rain
- Benjamín Celis
- Matías Sáez

## Sistema Web Ferremas

Este repositorio contiene el desarrollo completo del sistema Ferremas que hicimos para la evaluación 2 del ramo ASY5101. Usamos Java con Spring Boot para crear una API RESTful, conectada a una base de datos MySQL y documentada con Swagger. Todo el código está en la carpeta `miprimeraapi.zip`, y también subimos la base de datos, documentación y pruebas.

## Requisitos para ejecutar el sistema

### 1. Instalar XAMPP
- Descargar XAMPP desde: https://www.apachefriends.org/es/index.html
- Activar los módulos **Apache** y **MySQL**

### 2. Crear la base de datos
- Ir a [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
- Crear una nueva base de datos con el siguiente nombre:

miprimeraapi_db

> ⚠️ *No es necesario crear las tablas manualmente.*  
> Cuando corras el proyecto con Spring Boot, se crean solas gracias a la configuración de Hibernate.


## Cómo abrir y ejecutar el sistema

### 1. Visual Studio Code
- Abrir Visual Studio Code
- Instalar la extensión **Java Extension Pack** si no la tienes
- Descomprimir la carpeta `miprimeraapi.zip` y abrirla en VSCode

### 2. Verifica el archivo `application.properties`
Ubicado en:  
src/main/resources/application.properties


Debe tener esta configuración para conectarse con la base de datos local:

spring.datasource.url=jdbc:mysql://localhost:3306/miprimeraapi_db
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true


Cómo probar los endpoints
Swagger UI
Ir a: http://localhost:8080/swagger-ui/index.html

Aquí puedes ver y probar todos los endpoints de forma visual.

Postman
También puedes usar Postman para pruebas externas.

URL base: http://localhost:8080

Funcionalidades del sistema
Registro y búsqueda de productos

Validaciones (precio negativo, campos vacíos, etc.)

Historial de precios asociados a productos

Envío de mensajes por usuarios externos

Acceso restringido a mensajes solo para usuarios internos

Registro de usuarios con roles (interno y externo)

Simulación de pagos con WebPay

Conversión de divisa desde USD a CLP usando valores simulados

Consulta de transacciones de conversión realizadas
