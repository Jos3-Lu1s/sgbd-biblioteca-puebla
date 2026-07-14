# Simulación de Semilla de Base de Datos (prisma/semilla)

Este documento describe la lógica y los datos iniciales previstos para poblar (seeding) la base de datos PostgreSQL tras ejecutar las migraciones de Prisma.

## Propósito
- Crear cuentas administrativas iniciales necesarias para el primer ingreso al sistema.
- Cargar un catálogo inicial de categorías y libros base para demostración.
- Establecer configuraciones iniciales que permitan el correcto funcionamiento del software.

## Datos de Semilla Previstos

### 1. Usuarios Base
* **Administrador del Sistema:**
  - Nombre: "Administrador General SGBD"
  - Correo: `admin@sgbd-puebla.gob.mx`
  - Rol: `ADMIN`
* **Bibliotecario de Pruebas:**
  - Nombre: "Elena Pontiatowska (Bibliotecaria)"
  - Correo: `elena.biblio@sgbd-puebla.gob.mx`
  - Rol: `BIBLIOTECARIO`

### 2. Catálogos Iniciales
1. Ciencias Exactas
2. Historia de Puebla
3. Literatura Hispanoamericana

### 3. Libros de Muestra (Sembrados)
* **Categoría: Historia de Puebla**
  - Título: "La Batalla del 5 de Mayo: Crónica e Impacto"
  - Autor: "Jesús Anaya"
  - ISBN: "978-607-1234-01-2"
  - Copias: 5
* **Categoría: Literatura Hispanoamericana**
  - Título: "Ángeles del Abismo"
  - Autor: "Enrique Serna"
  - ISBN: "978-607-1234-02-9"
  - Copias: 3
* **Categoría: Ciencias Exactas**
  - Título: "Introducción a la Programación con JS"
  - Autor: "UTP Editorial"
  - ISBN: "978-607-1234-03-6"
  - Copias: 10

_Boceto de inicialización de datos para el flujo de Git — Sin código ejecutable._
