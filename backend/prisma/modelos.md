# Modelos previstos (Prisma)

Documento de trabajo de la rama `feature/backend-jose`. Describe, en texto y
no en código real, los modelos que más adelante se definirían en
`schema.prisma` sobre PostgreSQL. No se implementa el esquema real: es un
boceto de qué campos y relaciones tendría cada modelo.

## Usuario
- id, nombre, correo (único)
- rol: ADMIN, BIBLIOTECARIO o LECTOR

## Libro
- id, título, autor

## Catalogo
- id, nombre
- agrupa varios `Libro`

## Prestamo
- id, fecha
- relaciona un `Usuario` con un `Libro`

_Placeholder de estructura — sin implementación real, solo boceto de modelos._
