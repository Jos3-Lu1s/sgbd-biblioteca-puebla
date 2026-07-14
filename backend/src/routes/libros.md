# Rutas de Libros (routes/libros) - Simulación

Este documento describe la definición de los endpoints de la API dedicados a la gestión de libros dentro del catálogo de la biblioteca.

## Endpoints Previstos

### 1. Listar Libros
- **Método:** `GET`
- **Ruta:** `/api/libros`
- **Acceso:** Público (Lectores y visitantes)
- **Descripción:** Obtiene la lista completa de libros con soporte para filtros por título, autor y paginación.

### 2. Obtener Detalle de un Libro
- **Método:** `GET`
- **Ruta:** `/api/libros/:id`
- **Acceso:** Público
- **Descripción:** Devuelve la ficha bibliográfica detallada de un libro en específico.

### 3. Crear Libro
- **Método:** `POST`
- **Ruta:** `/api/libros`
- **Acceso:** Protegido (Solo ADMIN o BIBLIOTECARIO)
- **Descripción:** Registra un nuevo libro en la base de datos.

### 4. Actualizar Libro
- **Método:** `PUT`
- **Ruta:** `/api/libros/:id`
- **Acceso:** Protegido (Solo ADMIN o BIBLIOTECARIO)
- **Descripción:** Modifica los metadatos de un libro existente (título, autor, copias disponibles, etc.).

### 5. Eliminar Libro
- **Método:** `DELETE`
- **Ruta:** `/api/libros/:id`
- **Acceso:** Protegido (Solo ADMIN)
- **Descripción:** Elimina del catálogo la ficha del libro.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
