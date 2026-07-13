# Backend — SGBD API

API REST construida con **Express** siguiendo arquitectura **MVC**, con
**Prisma ORM** sobre **PostgreSQL** y autenticación basada en **JWT**.

## Estructura

- `src/config/` — configuración (base de datos, entorno, JWT)
- `src/models/` — modelos de datos (Prisma)
- `src/controllers/` — lógica de negocio por recurso
- `src/routes/` — definición de endpoints
- `src/services/` — lógica reutilizable / acceso a datos
- `src/middlewares/` — autenticación, validación, manejo de errores
- `src/utils/` — helpers generales
- `prisma/` — schema y migraciones de Prisma

_Placeholder — sin implementación real, solo estructura para Git._
