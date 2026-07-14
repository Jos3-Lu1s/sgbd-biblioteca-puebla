# Rutas de Usuarios (routes/usuarios) - Simulación

Este documento describe la definición de los endpoints de la API dedicados a la gestión de usuarios y autenticación.

## Endpoints Previstos

### 1. Iniciar Sesión (Login)
- **Método:** `POST`
- **Ruta:** `/api/usuarios/login`
- **Acceso:** Público
- **Descripción:** Valida credenciales de acceso y retorna un token JWT.

### 2. Registrar Lector
- **Método:** `POST`
- **Ruta:** `/api/usuarios/registro`
- **Acceso:** Público
- **Descripción:** Permite a nuevos usuarios registrarse como LECTORES.

### 3. Obtener Perfil
- **Método:** `GET`
- **Ruta:** `/api/usuarios/perfil`
- **Acceso:** Protegido (Requiere Token)
- **Descripción:** Retorna los datos del usuario logueado en base al token provisto.

### 4. Listar Usuarios
- **Método:** `GET`
- **Ruta:** `/api/usuarios`
- **Acceso:** Protegido (Requiere Token y rol de ADMIN o BIBLIOTECARIO)
- **Descripción:** Devuelve una lista de todos los usuarios registrados.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
