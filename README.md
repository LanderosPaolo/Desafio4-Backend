# Desafio4-Backend

Este repositorio contiene los siguientes archivos:

    consultas.js: Este archivo contiene las funciones de consulta a la base de datos PostgreSQL.
    server.js: Este archivo es el servidor Express que expone una API para interactuar con la base de datos.

Requisitos previos

Antes de ejecutar estos códigos, asegúrate de tener instalado lo siguiente:

    Node.js: Puedes descargarlo e instalarlo desde nodejs.org.
    PostgreSQL: Puedes descargar e instalar PostgreSQL desde postgresql.org y asegúrate de tener una base de datos creada.

Configuración

En el archivo consultas.js, debes proporcionar la configuración correcta de tu base de datos PostgreSQL en el objeto pool. Asegúrate de completar los siguientes campos:

    host: El host de tu base de datos, por ejemplo, "localhost" si está en tu máquina local.
    user: El nombre de usuario de tu base de datos.
    password: La contraseña de tu base de datos.
    database: El nombre de la base de datos que deseas utilizar.

Instalación

Sigue estos pasos para instalar y ejecutar el servidor:

    npm install

Una vez que se completen las instalaciones, puedes iniciar el servidor ejecutando el siguiente comando:

    npm run dev 
    o
    npm run start

    El servidor se ejecutará en el puerto 3000 por defecto.

Uso

El servidor proporciona los siguientes puntos finales de API:

    GET /posts: Obtiene todos los posts de la base de datos.
    POST /posts: Agrega un nuevo post a la base de datos. Debes proporcionar los campos titulo, img y descripcion en el cuerpo de la solicitud.
    PUT /posts/like/:id: Incrementa el contador de likes para un post específico identificado por su ID.
    DELETE /posts/:id: Elimina un post específico identificado por su ID.

Recuerda reemplazar :id con el ID real del post al hacer una solicitud PUT o DELETE.
Manejo de errores

El servidor maneja los siguientes casos de error:

    Si ocurre algún error interno del servidor, devolverá una respuesta con el código de estado 500 y un mensaje de error.
    Si se viola la restricción NOT NULL al agregar un post, devolverá una respuesta con el código de estado 400 y un mensaje específico de error.
    Si intentas eliminar un post que no existe, devolverá una respuesta con el código de estado 404 y un mensaje indicando que el recurso no se encontró.
