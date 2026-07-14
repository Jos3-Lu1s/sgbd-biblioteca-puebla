# Configuración del Sistema (config/configuracion) - Simulación

Este documento describe la estructura y configuración ambiental requerida para arrancar el backend del SGBD.

## Configuración y Entorno (.env)
Se definen las siguientes variables necesarias en el entorno de desarrollo y producción:
- `PORT`: Puerto donde se monta el servidor HTTP (por defecto `3000`).
- `DATABASE_URL`: URI de conexión a la base de datos PostgreSQL (ej. `postgresql://usuario:password@localhost:5432/sgbd`).
- `JWT_SECRET`: Llave secreta privada para la firma y verificación de tokens de autenticación JWT.
- `JWT_EXPIRES_IN`: Tiempo de expiración para las sesiones (ej. `24h` o `7d`).

## Conexión a Base de Datos (Prisma Client)
- Se prevé inicializar el cliente Prisma ORM en un archivo centralizado para que sea instanciado una sola vez en la aplicación.
- Configuración de logging de consultas SQL durante desarrollo para diagnóstico de rendimiento de base de datos.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
