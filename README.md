Task Manager API
================

Esta es una API para la gestión de tareas (To-Do List) utilizando Spring Boot como backend.

Requisitos
----------

* Java 17 (OpenJDK o cualquier distribución compatible)
* Maven 3.6+ (para construir y ejecutar el proyecto Spring Boot)

Configuración del Proyecto
--------------------------

### 1\. Clonar el Repositorio

    git clone https://github.com/jadruiz/task-manager-api.git

### 2\. Variables de Entorno

Usa el archivo `env.example` (localizado en la carpeta docs del proyecto) para establecer las variables de entorno.

Configuración y Ejecución de la API
-----------------------------------

### 1\. Compilar el Proyecto

Antes de ejecutar la API, asegúrate de compilar el proyecto usando Maven:

    cd task-manager-api
    mvn clean install

### 2\. Ejecutar la API

Para iniciar la aplicación, ejecuta el siguiente comando:

    mvn spring-boot:run

La API estará disponible en `http://localhost:8080`.

### 3\. Probar la API con Postman

Para probar la API, puedes usar Postman. Asegúrate de tener Postman instalado. Aquí están algunos ejemplos de cómo hacer solicitudes:

#### GET - Obtener todas las tareas

    GET {{base_url}}/api/tasks

#### POST - Crear una nueva tarea

    POST {{base_url}}/api/tasks

**Body (JSON):**

    {
        "title": "Nueva Tarea",
        "description": "Descripción de la tarea",
        "completed": false
    }

#### PUT - Actualizar una tarea

    PUT {{base_url}}/api/tasks/{id}

**Body (JSON):**

    {
        "title": "Tarea Actualizada",
        "description": "Descripción actualizada",
        "completed": true
    }

#### DELETE - Eliminar una tarea

    DELETE {{base_url}}/api/tasks/{id}

Archivo de Colección de Postman
-------------------------------

Si necesitas un archivo de colección de Postman para probar los endpoints, puedes encontrarlo en la carpeta `docs` del proyecto:

    docs/Todo Java Spring Boot.postman_collection.json

Importa este archivo en Postman para tener acceso a todas las solicitudes de la API preconfiguradas.

