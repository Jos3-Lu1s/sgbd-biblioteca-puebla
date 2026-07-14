# Rutas de Préstamos (routes/prestamos) - Simulación

Este documento describe la definición de los endpoints de la API dedicados a la gestión de préstamos virtuales de libros.

## Endpoints Previstos

### 1. Solicitar Préstamo
- **Método:** `POST`
- **Ruta:** `/api/prestamos`
- **Acceso:** Protegido (Cualquier usuario autenticado)
- **Descripción:** Registra la solicitud de préstamo de un libro para el usuario autenticado.

### 2. Listar Mis Préstamos
- **Método:** `GET`
- **Ruta:** `/api/prestamos/mis-prestamos`
- **Acceso:** Protegido (Cualquier usuario autenticado)
- **Descripción:** Obtiene el historial de préstamos del lector que realiza la petición.

### 3. Devolver Libro
- **Método:** `POST`
- **Ruta:** `/api/prestamos/:id/devolucion`
- **Acceso:** Protegido (Usuario del préstamo, ADMIN o BIBLIOTECARIO)
- **Descripción:** Finaliza el préstamo activo y marca el libro como devuelto.

### 4. Administrar Préstamos
- **Método:** `GET`
- **Ruta:** `/api/prestamos`
- **Acceso:** Protegido (Solo ADMIN o BIBLIOTECARIO)
- **Descripción:** Permite ver y filtrar todas las solicitudes de préstamo del sistema (activos, devueltos, vencidos).

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
