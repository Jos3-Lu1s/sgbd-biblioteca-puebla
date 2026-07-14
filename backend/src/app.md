# Servidor Express (app.js) - Simulación

Este documento describe la estructura y configuración que tendría el archivo `app.js` en el punto de entrada de la API REST del backend.

## Responsabilidades
- Cargar las variables de entorno (puerto, base de datos, secreto JWT).
- Configurar middlewares globales (`cors`, `express.json`).
- Registrar las rutas principales del sistema.
- Iniciar el servidor HTTP en el puerto correspondiente.

## Arquitectura Prevista
- **Ruta de Estado:** `GET /api/status` para monitorear la salud del servidor.
- **Ruta de Usuarios:** `use('/api/usuarios', usuarioRoutes)` mapeando las operaciones del usuario.
- **Manejo de Errores:** Middleware global para capturar errores HTTP y responder en formato JSON.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
