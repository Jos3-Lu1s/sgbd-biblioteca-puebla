# Utilidades Generales (utils/utilidades) - Simulación

Este documento describe los helpers o funciones utilitarias que asisten al flujo de peticiones dentro del backend.

## Utilidades Previstas

### 1. Formateador de Respuestas API (`responseFormatter`)
- Función para unificar la estructura de respuestas exitosas y de error enviadas al cliente React:
  ```json
  {
    "success": true,
    "data": { ... },
    "error": null,
    "timestamp": "2026-07-14T03:30:00Z"
  }
  ```

### 2. Generador y Validador de Contraseñas (`hashHelper`)
- Envoltura para las funciones de encriptación bcrypt, garantizando la seguridad en el hashing de contraseñas de los usuarios y su posterior cotejo en el login.

### 3. Manejador Personalizado de Errores (`AppError`)
- Clase que extiende la clase base de error de JavaScript para inyectar códigos de estado HTTP semánticos (ej. `400 Bad Request`, `404 Not Found`) y descripciones personalizadas.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
