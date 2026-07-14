# Controlador de Préstamos (controllers/prestamos) - Simulación

Este documento describe la lógica de control y validación de las transacciones de préstamos virtuales en el SGBD.

## Acciones y Lógica de Negocio

### `solicitarPrestamo(req, res)`
1. Extrae el `libroId` del cuerpo de la petición y el `usuarioId` de `req.usuario.id`.
2. Verifica si el libro existe y tiene copias físicas/licencias virtuales disponibles.
3. Comprueba si el lector tiene actualmente más de 3 préstamos activos o deudas de devoluciones atrasadas.
4. Genera un nuevo registro en la tabla `Prestamo` con la fecha actual y estado `ACTIVO`.
5. Reduce en 1 la disponibilidad del libro solicitado.
6. Retorna los detalles de la solicitud de préstamo aprobada.

### `listarMisPrestamos(req, res)`
1. Filtra los registros de `Prestamo` donde el ID del usuario coincida con `req.usuario.id`.
2. Devuelve la lista ordenada por fecha de solicitud, incluyendo información resumida del libro.

### `devolverLibro(req, res)`
1. Localiza el préstamo por el ID recibido en `req.params.id`.
2. Valida que el préstamo pertenezca al usuario logueado o que el solicitante sea `BIBLIOTECARIO`.
3. Cambia el estado del préstamo a `DEVUELTO` e inserta la fecha de retorno.
4. Aumenta en 1 la disponibilidad del libro.
5. Devuelve la confirmación de la devolución.

### `listarTodosLosPrestamos(req, res)`
1. Restringe el acceso si el rol del usuario no tiene permisos elevados.
2. Consulta todos los préstamos de la base de datos aplicando filtros como `estado` (ACTIVO, DEVUELTO, VENCIDO) y paginación.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
