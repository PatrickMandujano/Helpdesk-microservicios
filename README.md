# Backend - Plataforma web de helpdesk con microservicios

## Features

- Login para todos los usuarios
- CRUD completo de usuarios (dashboard de administrador)
- CRUD de equipos (dashboard de administrador)
- CRUD de componentes (dashboard de administrador)
- Crear y listar tickets (dashboard de administrador)
- Asignar tickets a técnicos (dashboard de administrador)
- Asociar ticket con usuario que reporta, prioridad y estado.
- Filtrar tickets por asunto, descripción, estado, prioridad y usuario que reporta.
- Panel de consulta de equipos (dashboard técnicos)
- Datatable de componentes (dashboard técnicos)
- Apertura de tickets y diagnóstico del técnico
- Consulta del estado de tickets para empleados

## Tech Stack

**Frontend:** 
<br/>
https://github.com/PatrickMandujano/Frontend-de-helpsdesk/tree/main
<br/>
<br/>
## ⚙️ Backend Tech Stack

El backend de **Helpdesk** está desarrollado con una arquitectura de microservicios basada en Java y Spring Boot. Utiliza Spring Cloud para el enrutamiento, descubrimiento de servicios y gestión centralizada de la configuración.

### 🛠️ Tecnologías principales

* **Java 17:** lenguaje de programación.
* **Spring Boot 3.4.6:** framework para el desarrollo de aplicaciones backend.
* **Spring Cloud 2024.0.2:** herramientas para implementar patrones de arquitectura distribuida.
* **Apache Maven:** construcción del proyecto y gestión de dependencias mediante un proyecto multimódulo.
* **MySQL:** sistema de gestión de bases de datos relacionales.

### 🏗️ Arquitectura y comunicación entre microservicios

* **Spring Cloud Gateway:** punto de entrada para el enrutamiento de solicitudes.
* **Netflix Eureka Server/Client:** registro y descubrimiento de servicios.
* **Spring Cloud Config Server:** gestión centralizada de la configuración.
* **Spring Cloud OpenFeign:** comunicación declarativa entre microservicios mediante clientes HTTP.

### 🗄️ Persistencia y acceso a datos

* **Spring Data JPA:** abstracción para el acceso y la persistencia de datos.
* **MySQL Connector/J:** controlador JDBC para la conexión con MySQL.
* **Hibernate:** proveedor JPA, sujeto a confirmación en las dependencias resueltas.

### 🔐 Seguridad y validación

* **Spring Security:** mecanismos de seguridad de la aplicación.
* **JSON Web Token (JWT):** gestión de tokens mediante JJWT.
* **Spring Boot Validation:** validación de datos de entrada.

### 📡 Desarrollo y documentación de API

* **Spring Web MVC:** desarrollo de servicios HTTP y API REST.
* **Spring WebFlux:** infraestructura reactiva utilizada por Spring Cloud Gateway.
* **Springdoc OpenAPI 2.5.0:** generación de documentación OpenAPI y Swagger UI.
* **Lombok:** reducción de código repetitivo en las clases Java.

### ⚙️ Configuración centralizada

El directorio `CONFIG-REPO` contiene archivos `.properties` con la configuración específica de los servicios.

* **API Gateway:** puerto, rutas de negocio y exposición de la documentación de las API.
* **User Management Service:** configuración de seguridad, JWT, Eureka y base de datos.
* **Helpdesk Ticket Service:** configuración de Eureka y conexión a MySQL.
* **Asset Management Service:** configuración de Eureka y conexión a MySQL.
* **Device Management Service:** configuración de Eureka y conexión a MySQL.

### 🧪 Testing

* **Spring Boot Starter Test:** dependencias de soporte para pruebas automatizadas.

### 📦 Microservicios

| Microservicio               | Responsabilidad                                 |
| --------------------------- | ----------------------------------------------- |
| `api-gateway`               | Enrutamiento de solicitudes hacia los servicios |
| `config-server`             | Gestión centralizada de la configuración        |
| `eureka-server`             | Registro y descubrimiento de servicios          |
| `user-management-service`   | Gestión de usuarios y autenticación             |
| `helpdesk-ticket-service`   | Gestión de tickets de soporte                   |
| `asset-management-service`  | Gestión de patrimonio                           |
| `device-management-service` | Gestión de dispositivos                         |

### 🗃️ Bases de datos

| Base de datos | Servicio asociado         |
| ------------- | ------------------------- |
| `users_db`    | User Management Service   |
| `tickets_db`  | Helpdesk Ticket Service   |
| `assets_db`   | Asset Management Service  |
| `devices_db`  | Device Management Service |
