# Controlador de Usuarios (controllers/usuarios) - Simulación

Este documento describe la lógica de control prevista para gestionar las solicitudes relacionadas con usuarios.

## Acciones y Lógica de Negocio

### `login(req, res)`
1. Valida la presencia de `correo` y `password` en el cuerpo de la petición.
2. Consulta el modelo de datos de `Usuario` para validar la existencia del correo.
3. Compara contraseñas usando encriptación hashes (ej. bcrypt).
4. Si las credenciales son válidas, firma y devuelve un token JWT con la información del `id` y `rol` del usuario.

### `registro(req, res)`
1. Valida que el `correo` no esté registrado previamente.
2. Encripta la contraseña elegida.
3. Inserta el nuevo usuario con rol por defecto de `LECTOR` en la base de datos PostgreSQL mediante Prisma.
4. Responde con el objeto de usuario creado.

### `obtenerPerfil(req, res)`
1. Utiliza el ID inyectado por el middleware de autenticación (`req.usuario.id`).
2. Consulta al modelo de datos para obtener la información de perfil actual del usuario.
3. Retorna la información al cliente.

### `listarUsuarios(req, res)`
1. Obtiene la lista completa de usuarios del sistema.
2. Aplica filtros y paginación si se especifican.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
