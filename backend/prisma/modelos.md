# Modelos previstos (Prisma)

Documento de trabajo de la rama `feature/backend-jose`. Describe, en texto y
no en código real, los modelos que más adelante se definirían en
`schema.prisma` sobre PostgreSQL. No se implementa el esquema real: es un
boceto de qué campos y relaciones tendría cada modelo.

## Usuario
- id (Int, PK)
- nombre (String)
- correo (String, único)
- password (String, encriptado)
- rol (Enum: ADMIN, BIBLIOTECARIO, LECTOR)
- activo (Boolean)

## Libro
- id (Int, PK)
- título (String)
- autor (String)
- isbn (String, único)
- copiasTotal (Int)
- copiasDisponibles (Int)

## Catalogo
- id (Int, PK)
- nombre (String, único)

## Prestamo
- id (Int, PK)
- usuarioId (Int, FK)
- libroId (Int, FK)
- fechaSolicitud (DateTime)
- fechaDevolucionLimite (DateTime)
- fechaDevolucionReal (DateTime)
- estado (Enum: ACTIVO, DEVUELTO, VENCIDO)

> [!NOTE]
> Para ver el diccionario de datos detallado con sus tipos y el diagrama Entidad-Relación, consulta [backend/src/models/entidades.md](file:///D:/Users/JoseLuis/Desktop/UTP/web/sgbd-biblioteca-puebla/backend/src/models/entidades.md).
