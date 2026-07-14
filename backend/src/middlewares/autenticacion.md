# Middleware de Autenticación (middlewares/autenticacion) - Simulación

Este documento describe la lógica y validación de seguridad implementada a través del middleware de token.

## Flujo del Middleware (`verificarToken`)

1. **Lectura de Cabecera:** Obtiene la cabecera `Authorization` de la petición HTTP.
2. **Validación de Formato:** Comprueba que comience con el esquema `Bearer <token>`.
3. **Validación de Token (JWT):** 
   - Extrae el token.
   - Verifica su integridad y firma usando la clave secreta configurada.
   - Valida que el token no haya expirado.
4. **Inyección en Petición:** Decodifica los datos del payload (como `id` y `rol`) y los inyecta en el objeto `req` como `req.usuario`.
5. **Control de Flujo:** Ejecuta `next()` si la verificación es exitosa. Si falla, interrumpe el flujo y responde inmediatamente con un error HTTP `401 Unauthorized` o `403 Forbidden`.

_Boceto de seguridad para el flujo de Git — Sin código ejecutable._
