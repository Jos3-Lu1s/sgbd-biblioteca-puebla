# Controlador de Libros (controllers/libros) - Simulación

Este documento describe la lógica de control y validación prevista para gestionar el catálogo de libros del SGBD.

## Acciones y Lógica de Negocio

### `listarLibros(req, res)`
1. Extrae los parámetros de búsqueda de la query (`titulo`, `autor`, `page`, `limit`).
2. Realiza una consulta filtrada en la tabla `Libro` utilizando Prisma ORM.
3. Devuelve los libros coincidentes y metadatos de paginación (total de páginas, página actual).

### `obtenerLibroPorId(req, res)`
1. Obtiene el ID del libro de la ruta (`req.params.id`).
2. Consulta el libro correspondiente en la base de datos.
3. Si el libro no existe, retorna un error `404 Not Found`.
4. Si existe, responde con los datos detallados del libro.

### `crearLibro(req, res)`
1. Verifica que el rol de la petición (`req.usuario.rol`) sea `ADMIN` o `BIBLIOTECARIO`.
2. Valida la presencia de campos obligatorios (`titulo`, `autor`).
3. Inserta el nuevo libro en la base de datos.
4. Responde con un estado `201 Created` y los datos del libro creado.

### `actualizarLibro(req, res)`
1. Verifica permisos de `ADMIN` o `BIBLIOTECARIO`.
2. Busca el libro por ID. Si no existe, retorna `404`.
3. Actualiza únicamente los campos provistos en el cuerpo de la petición.
4. Retorna el objeto actualizado.

### `eliminarLibro(req, res)`
1. Verifica permisos de `ADMIN`.
2. Valida que el libro no tenga préstamos activos asociados.
3. Elimina el registro físico o lógico (soft-delete) de la base de datos.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
