# Laboratorio 13: CRUD Completo con Spring Boot y SQL Server

Aplicación web de gestión de agenda de contactos desarrollada con **Spring Boot**, **Spring Data JPA**, **Thymeleaf** y persistencia en **SQL Server Express**.

## Arquitectura del Proyecto
* **Model (`com.gremio.lab13_crud.model`):** Entidad `Contacto` mapeada a la tabla `contacto`.
* **Repository (`com.gremio.lab13_crud.repository`):** Interfaz `ContactoRepository` extendiendo de `JpaRepository`.
* **Service (`com.gremio.lab13_crud.service`):** Clase `ContactoService` que encapsula la lógica de negocio y desacopla el controlador del acceso a datos.
* **Controller (`com.gremio.lab13_crud.controller`):** Controlador web `ContactoController` con rutas para listar, crear, editar y eliminar contactos.
* **Templates (`src/main/resources/templates`):** Vistas dinámicas `contactos.html` y `formulario.html` con Thymeleaf.

## Requisitos y Ejecución
1. Tener instalado **JDK** compatible con `pom.xml` y **SQL Server Express**.
2. Crear la base de datos `agenda` en SQL Server y habilitar el modo de autenticación mixto junto con TCP/IP en el puerto `1433`.
3. Configurar las credenciales de acceso en `src/main/resources/application.properties`.
4. Ejecutar el proyecto desde la raíz:
   ```bash
   ./mvnw spring-boot:run