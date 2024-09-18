  Task Manager API - README

Task Manager API
================

Esta es una API para la gestión de tareas (To-Do List) utilizando Spring Boot como backend y Angular 17 como frontend.

Requisitos
----------

*   Java 17 (OpenJDK o cualquier distribución compatible)
*   Maven 3.6+ (para construir y ejecutar el proyecto Spring Boot)
*   Node.js 18.x o superior (para el frontend Angular, opcional)
*   Postman (para probar los endpoints de la API, opcional)

Configuración del Proyecto
--------------------------

### 1\. Clonar el Repositorio

    git clone https://github.com/tu-usuario/task-manager-api.git

### 2\. Variables de Entorno

Crea un archivo `.env` en la raíz del proyecto backend y añade la variable de entorno para configurar CORS:

    CORS_ALLOWED_ORIGINS=http://localhost:4200

Esta variable define los orígenes permitidos para el intercambio de recursos entre dominios (CORS). Puedes cambiar este valor para permitir otros orígenes.

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

Configuración del Frontend (Opcional)
-------------------------------------

Si estás utilizando el frontend de Angular 17 para interactuar con la API, sigue estos pasos:

### 1\. Instalar las Dependencias

    cd frontend/todo-app
    npm install

### 2\. Ejecutar la Aplicación Angular

    ng serve

El frontend estará disponible en `http://localhost:4200`.

Archivo de Colección de Postman
-------------------------------

Si necesitas un archivo de colección de Postman para probar los endpoints, puedes encontrarlo en la carpeta `docs` del proyecto:

    docs/Todo Java Spring Boot.postman_collection.json

Importa este archivo en Postman para tener acceso a todas las solicitudes de la API preconfiguradas.

Notas Adicionales
-----------------

*   Asegúrate de tener el archivo `.env` correctamente configurado antes de ejecutar la aplicación.
*   Para cambiar la configuración de CORS, edita el valor de `CORS_ALLOWED_ORIGINS` en el archivo `.env`.
*   Para entornos de desarrollo y producción, ajusta las configuraciones según sea necesario.

Contacto
--------

Para más información o reportar problemas, contacta al desarrollador.